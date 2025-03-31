# 🖥️ PySide6 Cheat Sheet

PySide6 es el binding oficial de Qt para Python.

---

## 🚀 Instalación
```bash
pip install PySide6
```

## 📌 Crear una Ventana con PySide6
```python
from PySide6.QtWidgets import QApplication, QWidget

app = QApplication([])
ventana = QWidget()
ventana.setWindowTitle("Mi Aplicación PySide6")
ventana.setGeometry(100, 100, 400, 300)
ventana.show()
app.exec()
```

## 🎨 Widgets Básicos
```python
from PySide6.QtWidgets import QLabel, QPushButton, QVBoxLayout

layout = QVBoxLayout()
layout.addWidget(QLabel("¡Hola, PySide6!"))
layout.addWidget(QPushButton("Presiona"))

ventana.setLayout(layout)
```

## 📂 Diálogos y Mensajes
```python
from PySide6.QtWidgets import QMessageBox

QMessageBox.information(ventana, "Info", "Esto es un mensaje")
```

## 🔄 Eventos y Señales
```python
def on_click():
    print("Botón presionado")

btn = QPushButton("Clic")
btn.clicked.connect(on_click)
layout.addWidget(btn)
```

---

📌 **PySide6 es similar a PyQt6, pero con licencia libre.** 🚀
