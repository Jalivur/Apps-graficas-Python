# 🎮 Dear PyGui Cheat Sheet

Dear PyGui es una librería ultra rápida para interfaces interactivas en Python.

---

## 🚀 Instalación
```bash
pip install dearpygui
```

## 📌 Crear una Ventana con Dear PyGui
```python
import dearpygui.dearpygui as dpg

dpg.create_context()

with dpg.window(label="Ejemplo DPG"):
    dpg.add_text("¡Hola, Dear PyGui!")
    dpg.add_button(label="Presióname")

dpg.create_viewport(title='Mi Aplicación', width=600, height=400)
dpg.setup_dearpygui()
dpg.show_viewport()
dpg.start_dearpygui()
dpg.destroy_context()
```

## 🎨 Widgets Básicos
```python
with dpg.window(label="Mi Ventana"):
    dpg.add_slider_float(label="Ajuste", default_value=0.5)
    dpg.add_checkbox(label="Activar")

dpg.show_viewport()
```

## 📊 Gráficos y Tablas
```python
with dpg.window(label="Gráficos"):
    dpg.add_plot(label="Mi gráfico")

dpg.show_viewport()
```

---

📌 **Dear PyGui es rápido y está optimizado para gráficos interactivos.** 🚀
