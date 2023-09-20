import tkinter as tk

def open_second_page():
    # Destroy the current window and open the second page
    root.destroy()
    second_page()

def second_page():
    # Create a new window for the second page
    second_window = tk.Tk()
    second_window.title("Second Page")
    second_window.geometry("400x300")
    
    # Add content to the second page
    label = tk.Label(second_window, text="Welcome to the Second Page!", font=("Helvetica", 20))
    label.pack(pady=30)
    
    # Run the second page window
    second_window.mainloop()

# Create the main window
root = tk.Tk()
root.title("Attention Attention! - Hoda Taki, Jana Hoteit, Aya Eid")
root.geometry("400x300")
root.configure(bg="black")

# Add content to the main window
title_label = tk.Label(root, text="Attention Attention!", font=("Helvetica", 24), bg="black", fg="white")
title_label.pack(pady=50)

# Create a "Next" button
next_button = tk.Button(root, text="Next", command=open_second_page)
next_button.pack()

# Run the main window
root.mainloop()

