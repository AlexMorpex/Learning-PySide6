# Начало
## Устанавливаем и запускаем PySide6

pip install pyside6

.venv/Lib/site-packages/PySide6/designer.exe Открыть графический редактор

## Базовый файл main.py для запуска проекта

import sys

from PySide6.QtWidgets import QApplication, QMainWindow

from ui_main_window import Ui_MainWindow

class AppName(QMainWindow):

    def __init__(self):
    
        super(AppName, self).__init__()
        
        self.ui = Ui_MainWindow()
          
        self.ui.setupUi(self)


if __name__ == "__main__":

    app = QApplication(sys.argv)
    
    window = AppName()
    
    window.show()

    sys.exit(app.exec())
    
## Преобобразовать файлы ресурсов (qrc) и интерфейса (ui) в файл питона (py)

pysdie6-rcc < rc_название_.qrc > -o <rc_название_.py>

pyside6-uic <ui_название_.ui> -o <rc_название_.py>

# Логика приложения

## Работа с базой данных

Работа с базой данных в Qt осуществляется через QtSql

Создаём файл connection.py 
