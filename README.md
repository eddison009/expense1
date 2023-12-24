<h1>1.0 Constructing an Expense Tracker in Python using Object-Oriented Programming.</h1>

This initiative aims to develop an expense tracker employing Python's object-oriented programming principles.

Within this project, two classes were formulated: "Expense" and "ExpenseDatabase."

<h2>Expense Class</h2>
Encompassing methods such as __init__, update, and to_dict.

Methods:

**__init__(self, title, amount)**: Instigates an Expense object with a unique ID, title, amount, creation time, and update time.<br>
**update(self, title=None, amount=None)**: Amends the title and/or amount of the expense, adjusting the updated_at timestamp accordingly.<br>
**to_dict(self)**: Transforms the expense object into a dictionary format for facile serialization.<br>

<h2>ExpenseDatabase Class</h2>

Comprising methods such as __init__, add_expense, remove_expense, get_expense_by_id, get_expense_by_title, to_dict.

Methods:

__init__(self): Initializes an empty list to store expenses.<br>
**add_expense(self, expense)**: Appends a new expense object to the database.<br>
**remove_expense(self, expense_id)**: Eliminates an expense from the database based on its ID.<br>
**get_expense_by_id(self, expense_id)**: Retrieves an expense by its ID.<br>
**get_expense_by_title(self, expense_title)**: Retrieves a list of expenses with a given title.<br>
**to_dict(self)**: Converts the list of expenses into a dictionary format for straightforward serialization.<br>


<h2>Notes</h2>
The Expense class epitomizes individual expenses with unique IDs, titles, amounts, creation times, and update times.<br>
The ExpenseDatabase class oversees a list of expenses, facilitating addition, removal, and retrieval predicated on ID or title.<br>
The code employs UUID for unique identification, datetime for timestamp management, and dictionary formats for facile conversion and serialization.


<h1>2.0 Duplicating the Project</h1>

On GitHub, the repository is cloned utilizing the git clone command. This command is instrumental in generating a copy of a specific repository or branch within a repository.

Git, being a distributed version control system, maximizes the advantages of a full repository on an individual's machine through cloning.

<h2>Steps to Clone</h2>
The process to initiate a git clone.<br>
1. In the local machine, create a folder to clone the remote repository into using the command "mkdir {directory-name}" in Windows. First, set the terminal to the correct directory using "cd {directory-name}."<br>
Any terminal on the system can handle git provided it is installed. This includes Powershell, CommandPrompt, Git Bash, VS Code, and even Git GUI.<br>
2. Execute the git clone command to clone the repository into the created folder:

```git
git clone https://github.com/eddison009/expense1
```

When cloning a repository, the entire repository, including all files, branches, and commits, is obtained.

<p>Cloning a repository is typically a one-time action at the project's outset. Once a repository exists on a remote, such as on GitHub, it is cloned for local interaction. After cloning, regular development activities can be performed without the need for repeated cloning.</p>

<p>The ability to work with the entire repository allows developers to work freely, unconstrained by file limitations. Feature branches can be created for safe changes without restrictions on file access.</p>


<h1>3.0 How to Execute the Expense Tracker</h1>

The provided code serves as a script to showcase the functionality of an expense tracking system utilizing the **Expense** and **ExpenseDatabase** classes. The implementation is elucidated in segments for clarity. <br>

<h2> 3.1 Creating Expense Instances:</h2>

```python
expense_1 = Expense(title="fuel", amount=10000)
expense_2 = Expense(title="transport", amount=2000)
expense_3 = Expense(title="data", amount=1000)
expense_4 = Expense(title="food", amount=3000)
expense_5 = Expense(title="shoes", amount=10000)
expense_6 = Expense(title="shoes", amount=300000)
```

<h2>3.2 Creating ExpenseDatabase Instance:</h2>

```python
edb = ExpenseDatabase()
```

<h2>3.3 Adding Expenses to the Database:</h2>

```python
for expense in [expense_1, expense_2, expense_3, expense_4, expense_5, expense_6]:
    edb.add_expense(expense)
    print(edb.database)
    print()
    print("-" * 30)
    print()
```
This section of the code adds each expense to the **ExpenseDatabase** and prints the database after each addition.


<h2>3.4 Updating an Expense:</h2>

```python
print(expense_1.update(title="food", amount=5000))
```
This portion of the code updates expense_1 with a new title ("food") and amount (5000).

<h2>3.5 Removing an Expense</h2>

```python
print(edb.remove_expense(expense_id=expense_2.id))
```
This segment of the code removes the expense with **expense_2's ID** from the ExpenseDatabase.

<h2>3.6 Fetching an Expense by ID or Title:</h2>

```python
print(edb.get_expense_by_id(expense_id=expense_1.id))
print(edb.get_expense_by_title(expense_title="shoes"))
```
These lines retrieve an expense by its ID and title from the ExpenseDatabase.

<h2>3.7 Converting ExpenseDatabase to a dict of Dictionaries:</h2> 

```python
print(edb.to_dict())
```
This section of the code prints the ExpenseDatabase converted to a dictionary of dictionaries.

Note: The to_dict method is likely designed to convert the ExpenseDatabase contents into a dict of dictionaries for facile representation or serialization.

In essence, the code offers a fundamental illustration of expense management functionalities using the defined classes.
