# Tkinterstud
import tkinter as tk

#aqui é para funcionar
root = tk.Tk()
root.geometry('300x500')
root.title('Corazón')

def toggle_menu():
    
    def collapse_toggle_menu():
        toggle_menu_fn.destroy()
        toggle_btn.config(text='❤️️')
        toggle_btn.config(command=toggle_menu)

    toggle_menu_fn = tk.Frame(root, bg='#000000')
    
    home_btn= tk.Button(toggle_menu_fn, text='Home',
    font=('Arial', 20), bd=0, bg='#000000', fg='white',
    activebackground='#000000', activeforeground='red')
    home_btn.place(x=20, y=20)

    product_btn= tk.Button(toggle_menu_fn, text='produtos',
    font=('Arial', 20), bd=0, bg='#000000', fg='white',
    activebackground='#000000', activeforeground='red')
    product_btn.place(x=20, y=80)

    menu_btn= tk.Button(toggle_menu_fn, text='menu',
    font=('Arial', 20), bd=0, bg='#000000', fg='white',
    activebackground='#000000', activeforeground='red')
    menu_btn.place(x=20, y=140)

    contact_btn= tk.Button(toggle_menu_fn, text='Contato',
    font=('Arial', 20), bd=0, bg='#000000', fg='white',
    activebackground='#000000', activeforeground='red')
    contact_btn.place(x=20, y=200)

    feedback_btn= tk.Button(toggle_menu_fn, text='feedback',
    font=('Arial', 20), bd=0, bg='#000000', fg='white',
    activebackground='#000000', activeforeground='red')
    feedback_btn.place(x=20, y=260)

    about_btn= tk.Button(toggle_menu_fn, text='Saiba mais',
    font=('Arial', 20), bd=0, bg='#000000', fg='white',
    activebackground='#000000', activeforeground='red')
    about_btn.place(x=20, y=320)

    window_heigth = root.winfo_height()
    
    toggle_menu_fn.place(x=0, y=50, height =window_heigth, width=200)

    toggle_btn.config(text='💔')
    toggle_btn.config(command=collapse_toggle_menu)

#aqui é a Header
head_frame = tk.Frame(root, bg='#000000',
highlightbackground='white', highlightthickness=1)

#Aqui é o botao esquerdo
toggle_btn = tk.Button(head_frame, text='❤️️', bg='#000000', fg='red', 
font=('Bold', 20), bd=0, activebackground='#000000', activeforeground='white',
command=toggle_menu)

toggle_btn.pack(side=tk.LEFT)

#aqui o titulo da header
title_lb = tk.Label(head_frame, text='Corazón', bg='#000000', fg='white',
font=('Arial', 20))
title_lb.pack(side=tk.LEFT)

#Variavel de header
head_frame.pack(side=tk.TOP, fill=tk.X)
head_frame.pack_propagate(False)
head_frame.configure(height = 50)


root.mainloop()
