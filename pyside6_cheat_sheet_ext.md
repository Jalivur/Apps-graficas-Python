# 🖥️ PySide6 Cheat Sheet (Avanzado)

PySide6 es un binding de Qt para Python que permite crear interfaces gráficas modernas.

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
from PySide6.QtWidgets import QLabel, QPushButton, QLineEdit, QTextEdit, QVBoxLayout

layout = QVBoxLayout()
layout.addWidget(QLabel("¡Hola, PySide6!"))
layout.addWidget(QPushButton("Presiona"))
layout.addWidget(QLineEdit("Entrada de texto"))
layout.addWidget(QTextEdit("Área de texto"))

ventana.setLayout(layout)
```

## 📦 Layouts Avanzados
```python
from PySide6.QtWidgets import QHBoxLayout

h_layout = QHBoxLayout()
h_layout.addWidget(QPushButton("Izquierda"))
h_layout.addWidget(QPushButton("Derecha"))

layout.addLayout(h_layout)
```

## 📂 Diálogos y Mensajes
```python
from PySide6.QtWidgets import QFileDialog, QMessageBox

QMessageBox.information(ventana, "Info", "Esto es un mensaje")
file, _ = QFileDialog.getOpenFileName(ventana, "Abrir archivo")
```

## 🔄 Eventos y Señales
```python
def on_click():
    print("Botón presionado")

btn = QPushButton("Clic")
btn.clicked.connect(on_click)
layout.addWidget(btn)
```

## 🎨 Estilos con CSS
```python
ventana.setStyleSheet("background-color: lightgray;")
btn.setStyleSheet("color: white; background-color: blue;")
```

---

📌 **PySide6 es ideal para interfaces modernas y personalizables.** 🚀
