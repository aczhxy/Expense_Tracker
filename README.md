# Expense_Tracker

class ExpenseTracker:
    
    def __init__(self):
        
        self.expenses = {
            
            "home": 0,
            
            "misc": 0,
            
            "food": 0,
            
            "work": 0,
            
            "fun": 0
        }
        

    def get_total(self):
    
        total = 0
        
        for category, amount in self.expenses.items():
        
            total += amount
 
        return total
  
    def get_expenses_by_category(self, category):
   
        return self.expenses[category]
    
    def update_expense(self, category):
    
        amount = float(input(f"Enter expense for {category}: "))
        
        self.expenses[category] = amount
    
    def display_expenses(self):
    
        for category, amount in self.expenses.items():
         
            print(f"{category}: {amount}")
            

tracker = ExpenseTracker()

while True:

    print("1. Update expenses")
    
    print("2. Get total expenses")
    
    print("3. Get expenses by category")
    
    print("4. Display all expenses")
    
    print("5. Exit")
    
    choice = input("Choose an option: ")
    
    if choice == "1":
    
        for category in tracker.expenses.keys():
        
            tracker.update_expense(category)
    
    elif choice == "2":
    
        print(f"Total expenses: {tracker.get_total()}")
    
    elif choice == "3":
    
        category = input("Enter category: ")
        
        if category.lower() in ["home", "misc", "food", "work", "fun"]:
        
            print(f"Expenses in {category}: {tracker.get_expenses_by_category(category)}")
        
        else:
        
            print("Invalid category. Please choose from home, misc, food, work, or fun.")
    
    elif choice == "4":
    
        tracker.display_expenses()
   
    elif choice == "5":
    
        break
    
    else:
    
        print("Invalid option. Please choose again.")
        
![image](https://github.com/user-attachments/assets/04f5434c-0480-4323-bc3c-689b8fb5e01a)
