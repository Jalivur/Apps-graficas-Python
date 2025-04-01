# 🖥️ PySide6 Cheat Sheet

## 📌 ¿Qué es PySide6?
PySide6 es un binding de la biblioteca Qt para Python que permite crear interfaces gráficas modernas y multiplataforma.

---

## 🚀 Instalación
```bash
pip install PySide6
```

## 📌 Estructura Básica de una Aplicación
```python
from PySide6.QtWidgets import QApplication, QWidget

app = QApplication([])  # Inicializa la aplicación
ventana = QWidget()  # Crea una ventana
ventana.setWindowTitle("Mi Aplicación PySide6")
ventana.setGeometry(100, 100, 400, 300)  # Posición y tamaño
ventana.show()  # Muestra la ventana
app.exec()  # Ejecuta el bucle de eventos
```

## 🎨 Widgets y Controles
### 🔹 Etiquetas y Botones
```python
from PySide6.QtWidgets import QLabel, QPushButton

label = QLabel("¡Hola, PySide6!", ventana)
label.move(20, 20)

btn = QPushButton("Presiona", ventana)
btn.move(20, 50)
```

### 🔹 Entradas de Texto
```python
from PySide6.QtWidgets import QLineEdit

entrada = QLineEdit(ventana)
entrada.setPlaceholderText("Escribe aquí...")
entrada.move(20, 80)
```

### 🔹 Áreas de Texto y Listas
```python
from PySide6.QtWidgets import QTextEdit, QListWidget

texto = QTextEdit(ventana)
texto.setText("Texto de ejemplo")
texto.move(20, 110)

lista = QListWidget(ventana)
lista.addItems(["Elemento 1", "Elemento 2", "Elemento 3"])
lista.move(20, 200)
```

## 📦 Organización con Layouts
```python
from PySide6.QtWidgets import QVBoxLayout

layout = QVBoxLayout()
layout.addWidget(label)
layout.addWidget(btn)
layout.addWidget(entrada)

ventana.setLayout(layout)
```

## 🔄 Eventos y Señales
```python
def on_click():
    label.setText("¡Botón presionado!")

btn.clicked.connect(on_click)
```

## 🎨 Personalización y Estilos
```python
ventana.setStyleSheet("background-color: #f0f0f0;")
btn.setStyleSheet("color: white; background-color: blue;")
```

## 📑 Diálogos y Mensajes
```python
from PySide6.QtWidgets import QMessageBox

QMessageBox.information(ventana, "Info", "Esto es un mensaje")
```

## 📂 Abrir y Guardar Archivos
```python
from PySide6.QtWidgets import QFileDialog

archivo, _ = QFileDialog.getOpenFileName(ventana, "Abrir Archivo")
```

---

📌 **PySide6 es ideal para interfaces modernas y avanzadas.** 🚀
