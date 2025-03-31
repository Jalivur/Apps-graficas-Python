# 🖥️ PyQt6 Cheat Sheet

PyQt6 es un binding de la biblioteca Qt para crear interfaces gráficas en Python.

---

## 🚀 Instalación
```bash
pip install PyQt6
```

## 📌 Crear una Ventana con PyQt6
```python
from PyQt6.QtWidgets import QApplication, QWidget

app = QApplication([])
ventana = QWidget()
ventana.setWindowTitle("Mi Aplicación PyQt6")
ventana.setGeometry(100, 100, 400, 300)
ventana.show()
app.exec()
```

## 🎨 Widgets Básicos
```python
from PyQt6.QtWidgets import QLabel, QPushButton, QVBoxLayout

layout = QVBoxLayout()
layout.addWidget(QLabel("¡Hola, PyQt6!"))
layout.addWidget(QPushButton("Presiona"))

ventana.setLayout(layout)
```

## 📂 Diálogos y Mensajes
```python
from PyQt6.QtWidgets import QMessageBox

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

## 📑 Diseñador de Interfaces (Qt Designer)
```bash
pip install pyqt6-tools
designer  # Ejecutar Qt Designer
```

---

📌 **PyQt6 es ideal para interfaces avanzadas y personalizables.** 🚀
