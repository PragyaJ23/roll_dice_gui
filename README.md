# roll_dice_gui
import tkinter as tk
import random

def roll_dice():
    dice_value=random.randint(1,6)
    label_result.config(text=f"You rolled: {dice_value}")
    dice_label.config(text=dice_unicode[dice_value])

#unicode characters for dice faces

dice_unicode={
    1:"\u2680",
    2:"\u2681",
    3:"\u2682",
    4:"\u2683",
    5:"\u2684",
    6:"\u2685"
}

# Create main window

root=tk.Tk()
root.title("Dice Roller")
root.geometry("300x200")

#dice face display

dice_label = tk.Label(root, text="", font=("Helvetica", 100))
dice_label.pack()

#result text display

label_result = tk.Label(root, text="Click the button to roll the dice!", font=("Helvetica", 14))
label_result.pack(pady=10)

# Button to roll the dice
roll_button = tk.Button(root, text="Roll Dice", command=roll_dice, font=("Helvetica", 12), bg="green", fg="white")
roll_button.pack()

#run the GUI loop

root.mainloop()



