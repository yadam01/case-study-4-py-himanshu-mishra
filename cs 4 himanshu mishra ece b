def display_menu():
    print("1. Add Task")
    print("2. View Tasks")
    print("3. Delete Task")
    print("4. Mark Task as Completed")
    print("5. Exit")

def add_task(tasks):
    task = input("Write the task: ")
    tasks.append({"task": task, "completed": False})
    print("Task added.")

def view_tasks(tasks):
    if len(tasks) == 0:
        print("No tasks available.")
        return
    index = 0
    while index < len(tasks):
        task = tasks[index]
        status = "Done" if task["completed"] else "Pending"
        print(str(index + 1) + ". " + task["task"] + " [" + status + "]")
        index += 1

def delete_task(tasks):
    view_tasks(tasks)
    if len(tasks) == 0:
        return
    num = input("Which task to delete (enter number): ")
    if num.isdigit():
        num = int(num)
        if num >= 1 and num <= len(tasks):
            removed = tasks[num - 1]["task"]
            tasks.pop(num - 1)
            print("Removed: " + removed)
        else:
            print("Invalid task number.")
    else:
        print("Please enter a number.")

def mark_completed(tasks):
    view_tasks(tasks)
    if len(tasks) == 0:
        return
    num = input("Which task to mark as completed (enter number): ")
    if num.isdigit():
        num = int(num)
        if num >= 1 and num <= len(tasks):
            tasks[num - 1]["completed"] = True
            print("Task marked as completed.")
        else:
            print("Invalid task number.")
    else:
        print("Please enter a number.")

def main():
    tasks = []
    while True:
        display_menu()
        choice = input("Choose an option: ")
        if choice == "1":
            add_task(tasks)
        elif choice == "2":
            view_tasks(tasks)
        elif choice == "3":
            delete_task(tasks)
        elif choice == "4":
            mark_completed(tasks)
        elif choice == "5":
            print("Exiting.")
            break
        else:
            print("Invalid option. Try again.")

main()
