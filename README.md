#program to calculate library charges
Def calculate_fine(book_id, due_date, return_date):
  
    Due_date = datetime.strptime(due_date, ‘%Y-%m-%d’)
    Return_date = datetime.strptime(return_date, ‘%Y-%m-%d’)
    Days_overdue = (return_date – due_date).days
    
    If days_overdue <= 7:
        Fine_rate = 20
    Elif days_overdue <= 14:
        Fine_rate = 50
    Else:
        Fine_rate = 100
    Fine_amount = fine_rate * days_overdue
    
    Print(“Book ID:”, book_id)
    Print(“Due Date:”, due_date.strftime(‘%Y-%m-%d’)) 
    Print(“Return Date:”, return_date.strftime(‘%Y-%m-%d’))
    Print(“Days Overdue:”, days_overdue)
    Print(“Fine Rate:”, fine_rate)
    Print(“Fine Amount:”, fine_amount)
 
Book_id = input(“Enter Book ID: “)
Due_date = input(“Enter Due Date (YYYY-MM-DD): “)
Return_date = input(“Enter Return Date (YYYY-MM-DD): “)

Calculate_fine(book_id, due_date, return_date)

