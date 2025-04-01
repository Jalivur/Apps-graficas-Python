# 🎮 Dear PyGui Cheat Sheet

## 📌 ¿Qué es Dear PyGui?
Dear PyGui es una librería ultrarrápida para interfaces gráficas en Python, basada en OpenGL.

---

## 🚀 Instalación
```bash
pip install dearpygui
```

## 📌 Estructura Básica de una Aplicación
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

## 🎨 Widgets y Controles
```python
with dpg.window(label="Mi Ventana"):
    dpg.add_slider_float(label="Ajuste", default_value=0.5)
    dpg.add_checkbox(label="Activar")
```

## 📊 Gráficos y Tablas
```python
with dpg.window(label="Gráficos"):
    dpg.add_plot(label="Mi gráfico")
```

## 🎨 Personalización de Tema
```python
dpg.add_theme_color(dpg.mvThemeCol_Button, (0, 100, 200, 255))
```

---

📌 **Dear PyGui es rápido y está optimizado para gráficos interactivos.** 🚀
