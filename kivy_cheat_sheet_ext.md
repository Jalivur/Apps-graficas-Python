# 📱 Kivy Cheat Sheet (Avanzado)

Kivy es un framework para crear apps en Windows, Linux, Mac, Android e iOS.

---

## 🚀 Instalación
```bash
pip install kivy
```

## 📌 Crear una Ventana con Kivy
```python
from kivy.app import App
from kivy.uix.label import Label

class MyApp(App):
    def build(self):
        return Label(text="¡Hola, Kivy!")

MyApp().run()
```

## 🎨 Widgets Básicos
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

## 📑 Archivos KV (Separación de Diseño y Lógica)
```kv
<MyWidget>:
    Label:
        text: "¡Hola desde KV!"
```

## 🔄 Eventos y Animaciones
```python
btn = Button(text="Presiona")

def on_press(instance):
    print("Botón presionado")

btn.bind(on_press=on_press)
layout.add_widget(btn)
```

## 🎨 Estilos y Temas
```python
from kivy.core.window import Window

Window.clearcolor = (1, 1, 1, 1)  # Fondo blanco
btn.background_color = (0, 0, 1, 1)  # Azul
```

---

📌 **Kivy es ideal para apps móviles y pantallas táctiles.** 🚀
