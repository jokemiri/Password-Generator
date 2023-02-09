import random
from tkinter import * #import the entire tkinter module for gui
import string #import the inbuilt string module
import pyperclip
def keygen():
    lcase=string.ascii_lowercase #variable to store small letters
    ucase=string.ascii_uppercase #variable to store CAPITAL letters
    numbs=string.digits #variable to store numbers
    spexter=string.punctuation #variable to store special charaters
    letters=lcase+ucase #variable to store only alphabets
    alphanum=lcase+ucase+numbs #variable to store only alphanumeric keys
    pword=lcase+ucase+numbs+spexter #variable to store all characters

    pword_length=int(lengthSelector.get())

    if choice.get()==1:
        passwordField.insert(0,random.sample(letters, pword_length))

    if choice.get()==2:
        passwordField.insert(0,random.sample(alphanum, pword_length))

    if choice.get()==3:
        passwordField.insert(0,random.sample(pword, pword_length))
    # password=random.sample(pword, pword_length)
    # passwordField.insert(0,password)

def copy():
    generated_password=passwordField.get()
    pyperclip.copy(generated_password)

root=Tk() #call the Tk class from the tkinter module
root.config(bg="black") #define the background colour
choice=IntVar()
selectFont=("steelfish eb", 12, "bold") #define font properties for the selectors
spinboxFont=("Cambria", 10, "bold") #define font properties for the spinbox
generateFont=("Cambria", 14, "bold") #define font properties for the generate button
passwordFont=("Cambria", 12) #define font properties for the generated password

appLabel=Label(root, text="Ojolimi KeyGen", font=("steelfish eb", 18, "bold"), bg="black", fg="white")
appLabel.grid(pady=10)

weakSelect=Radiobutton(root, text="Weak", value=1, variable=choice, font=selectFont)
weakSelect.grid(pady=3)

mediumSelect=Radiobutton(root, text="Medium", value=2, variable=choice, font=selectFont)
mediumSelect.grid(pady=3)

strongSelect=Radiobutton(root, text="Strong", value=3, variable=choice, font=selectFont)
strongSelect.grid(pady=3)

lengthLabel=Label(root, text="Select Length", font=("steelfish eb", 16, "bold"), bg="black", fg="white")
lengthLabel.grid()

lengthSelector=Spinbox(root, from_=5, to_=18, width=5, font=spinboxFont)
lengthSelector.grid()

generateButton=Button(root, text="Generate", font=generateFont, border=2, command=keygen)
generateButton.grid(pady=5)

passwordField=Entry(root, width=40, bd=2, font=passwordFont)
passwordField.grid(pady=3)

copyButton=Button(root, text="Copy", font=generateFont, command=copy)
copyButton.grid(pady=5)
root.mainloop()