# 📱 Kivy Cheat Sheet

## 📌 ¿Qué es Kivy?
Kivy es un framework para crear aplicaciones gráficas en Windows, Mac, Linux, Android e iOS.

---

## 🚀 Instalación
```bash
pip install kivy
```

## 📌 Estructura Básica de una Aplicación
```python
from kivy.app import App
from kivy.uix.label import Label

class MyApp(App):
    def build(self):
        return Label(text="¡Hola, Kivy!")

MyApp().run()
```

## 🎨 Widgets y Controles
### 🔹 Botones y Etiquetas
```python
from kivy.uix.button import Button
from kivy.uix.boxlayout import BoxLayout

layout = BoxLayout()
layout.add_widget(Label(text="Texto en Kivy"))
layout.add_widget(Button(text="Botón"))

class MyApp(App):
    def build(self):
        return layout

MyApp().run()
```

### 🔹 Entradas de Texto y Listas
```python
from kivy.uix.textinput import TextInput

entrada = TextInput(text="Escribe aquí")
```

## 📦 Organización con Layouts
```python
from kivy.uix.gridlayout import GridLayout

layout = GridLayout(cols=2)
layout.add_widget(Label(text="Nombre:"))
layout.add_widget(TextInput())
```

## 🔄 Eventos y Animaciones
```python
btn = Button(text="Presiona")

def on_press(instance):
    print("Botón presionado")

btn.bind(on_press=on_press)
```

## 🎨 Personalización y Estilos
```python
from kivy.core.window import Window

Window.clearcolor = (1, 1, 1, 1)  # Fondo blanco
```

---

📌 **Kivy es ideal para apps móviles y pantallas táctiles.** 🚀
