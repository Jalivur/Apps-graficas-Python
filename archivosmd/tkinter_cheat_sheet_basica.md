# 📜 Tkinter Cheat Sheet (Python)

Tkinter es la biblioteca estándar de Python para crear interfaces gráficas (GUI).

---

## 🛠️ Importar Tkinter
```python
import tkinter as tk
from tkinter import ttk  # Para widgets mejorados
from tkinter import messagebox, filedialog  # Para diálogos
```

---

## 📌 Crear una Ventana
```python
root = tk.Tk()
root.title("Mi Aplicación")
root.geometry("400x300")  # Ancho x Alto
root.mainloop()  # Iniciar la GUI
```

---

## 🎨 Widgets Básicos

### 📍 Etiqueta (Label)
```python
label = tk.Label(root, text="¡Hola, Tkinter!")
label.pack()
```

### 📝 Entrada de Texto (Entry)
```python
entry = tk.Entry(root)
entry.pack()
```

### 🔘 Botón (Button)
```python
def say_hello():
    print("Hola!")

btn = tk.Button(root, text="Saludar", command=say_hello)
btn.pack()
```

### 📌 Botón de Radio (Radiobutton)
```python
var = tk.StringVar(value="Opción 1")

radio1 = tk.Radiobutton(root, text="Opción 1", variable=var, value="Opción 1")
radio2 = tk.Radiobutton(root, text="Opción 2", variable=var, value="Opción 2")

radio1.pack()
radio2.pack()
```

### ✅ Casilla de Verificación (Checkbutton)
```python
var_check = tk.BooleanVar()

check = tk.Checkbutton(root, text="Acepto términos", variable=var_check)
check.pack()
```

### 📜 Área de Texto (Text)
```python
text_area = tk.Text(root, height=5, width=30)
text_area.pack()
```

### 📊 Barra de Progreso (Progressbar)
```python
progress = ttk.Progressbar(root, length=200, mode='determinate')
progress.pack()
progress.start(10)  # Iniciar progreso
```

---

## 📦 Organización de Widgets

### 📍 `pack()`
```python
widget.pack(side="top", fill="both", expand=True)
```

### 📍 `grid()`
```python
widget.grid(row=0, column=1, padx=5, pady=5)
```

### 📍 `place()`
```python
widget.place(x=50, y=100)
```

---

## 📂 Diálogos y Mensajes

### 📩 Cuadro de Mensaje
```python
messagebox.showinfo("Título", "Este es un mensaje")
```

### 📁 Abrir Archivo
```python
file = filedialog.askopenfilename()
print(file)
```

### 📁 Guardar Archivo
```python
file = filedialog.asksaveasfilename(defaultextension=".txt")
print(file)
```

---

## 📅 Widgets Avanzados

### 📑 Pestañas con `Notebook`
```python
notebook = ttk.Notebook(root)

tab1 = ttk.Frame(notebook)
tab2 = ttk.Frame(notebook)

notebook.add(tab1, text="Pestaña 1")
notebook.add(tab2, text="Pestaña 2")

notebook.pack(expand=True, fill="both")
```

### 📋 Menú Desplegable (Combobox)
```python
combo = ttk.Combobox(root, values=["Opción 1", "Opción 2", "Opción 3"])
combo.pack()
combo.current(0)  # Seleccionar primer valor
```

### 📜 Listbox (Lista de Elementos)
```python
listbox = tk.Listbox(root)
listbox.pack()

listbox.insert(1, "Elemento 1")
listbox.insert(2, "Elemento 2")
```

---

## 🔄 Eventos y Enlaces
```python
def on_key(event):
    print(f"Tecla presionada: {event.keysym}")

root.bind("<KeyPress>", on_key)
```

---

## 🔳 Canvas (Dibujos y Gráficos)
```python
canvas = tk.Canvas(root, width=200, height=200, bg="white")
canvas.pack()

canvas.create_rectangle(50, 50, 150, 150, fill="blue")
```

---

## 🏁 Ejecutar el Bucle de la Aplicación
```python
root.mainloop()
```

---

Este cheat sheet cubre lo esencial para empezar con **Tkinter** en Python. 🚀
