# 🖥️ PySide6 Cheat Sheet - Guía Completa y Avanzada

## 📌 ¿Qué es PySide6?
PySide6 es un binding oficial de la biblioteca Qt para Python que permite crear interfaces gráficas modernas, altamente personalizables y multiplataforma. Proporciona herramientas avanzadas para diseñar aplicaciones con estilos visuales atractivos y una experiencia de usuario optimizada.

---

## 🚀 Instalación
```bash
pip install PySide6
```

---

## 🏗️ Estructura Básica de una Aplicación
```python
from PySide6.QtWidgets import QApplication, QWidget

app = QApplication([])  # Inicializa la aplicación
ventana = QWidget()  # Crea una ventana
ventana.setWindowTitle("Mi Aplicación PySide6")
ventana.setGeometry(100, 100, 400, 300)  # Posición y tamaño
ventana.show()  # Muestra la ventana
app.exec()  # Ejecuta el bucle de eventos
```

---

## 🎨 Widgets y Controles

### 🔹 Etiquetas y Botones
```python
from PySide6.QtWidgets import QLabel, QPushButton

label = QLabel("¡Hola, PySide6!", ventana)
label.move(20, 20)

btn = QPushButton("Presiona", ventana)
btn.move(20, 50)
```

### 🔹 Entradas de Texto y Campos de Contraseña
```python
from PySide6.QtWidgets import QLineEdit

entrada = QLineEdit(ventana)
entrada.setPlaceholderText("Escribe aquí...")
entrada.move(20, 80)

entrada_password = QLineEdit(ventana)
entrada_password.setEchoMode(QLineEdit.Password)  # Oculta la contraseña
entrada_password.move(20, 110)
```

### 🔹 Botones con Iconos y Tooltips
```python
from PySide6.QtGui import QIcon

btn.setIcon(QIcon("icono.png"))
btn.setToolTip("Este es un botón con icono")
```

### 🔹 Menús y Barras de Herramientas
```python
from PySide6.QtWidgets import QMainWindow, QMenuBar

class MainWindow(QMainWindow):
    def __init__(self):
        super().__init__()
        self.setWindowTitle("Menú en PySide6")
        menu_bar = QMenuBar(self)
        archivo_menu = menu_bar.addMenu("Archivo")
        self.setMenuBar(menu_bar)
```

---

## 📦 Organización con Layouts

### 🔹 QVBoxLayout para distribución vertical
```python
from PySide6.QtWidgets import QVBoxLayout

layout = QVBoxLayout()
layout.addWidget(label)
layout.addWidget(btn)
layout.addWidget(entrada)

ventana.setLayout(layout)
```

### 🔹 QGridLayout para estructuras más complejas
```python
from PySide6.QtWidgets import QGridLayout

layout = QGridLayout()
layout.addWidget(label, 0, 0)
layout.addWidget(entrada, 0, 1)
layout.addWidget(btn, 1, 0, 1, 2)

ventana.setLayout(layout)
```

---

## 🎨 Personalización y Estilos

### 🔹 Cambiar colores y estilos con CSS
```python
ventana.setStyleSheet("background-color: #f0f0f0;")
btn.setStyleSheet("color: white; background-color: blue; border-radius: 10px; padding: 5px;")
```

### 🔹 Aplicar un tema oscuro
```python
app.setStyleSheet('''
    QWidget {
        background-color: #121212;
        color: #ffffff;
        font-size: 14px;
    }
    QPushButton {
        background-color: #1f1f1f;
        border: 1px solid #555;
        padding: 8px;
        border-radius: 5px;
    }
    QPushButton:hover {
        background-color: #333;
    }
''')
```

### 🔹 Aplicar bordes redondeados y sombras
```python
entrada.setStyleSheet("border: 2px solid #0078D7; padding: 5px; border-radius: 5px;")
```

### 🔹 Gradientes de Fondo
```python
ventana.setStyleSheet("background: qlineargradient(spread:pad, x1:0, y1:0, x2:1, y2:1, stop:0 #ff7e5f, stop:1 #feb47b);")
```

### 🔹 Agregar imágenes de fondo
```python
ventana.setStyleSheet("background-image: url('fondo.jpg'); background-repeat: no-repeat; background-position: center;")
```

---

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

## 🎭 Uso de Iconos y Fuentes Personalizadas
```python
from PySide6.QtGui import QIcon, QFont

ventana.setWindowIcon(QIcon("icono.png"))
ventana.setFont(QFont("Arial", 12))
```

## 🎬 Animaciones y Efectos

### 🔹 Movimiento Animado
```python
from PySide6.QtCore import QPropertyAnimation, QRect

animacion = QPropertyAnimation(ventana, b"geometry")
animacion.setDuration(1000)
animacion.setStartValue(QRect(100, 100, 400, 300))
animacion.setEndValue(QRect(200, 200, 600, 400))
animacion.start()
```

### 🔹 Desvanecimiento de un Widget
```python
from PySide6.QtCore import QPropertyAnimation
from PySide6.QtWidgets import QLabel

label = QLabel("Desvaneciéndose", ventana)
animacion = QPropertyAnimation(label, b"windowOpacity")
animacion.setDuration(2000)
animacion.setStartValue(1.0)
animacion.setEndValue(0.0)
animacion.start()
```

---

📌 **PySide6 ofrece herramientas avanzadas para diseñar interfaces modernas, dinámicas y altamente personalizadas.** 🚀
