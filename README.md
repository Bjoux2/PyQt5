# PyQt5

## QGraphicsView 图片显示逻辑

### 1

' photo = QtWidgets.QGraphicsPixmapItem().setPixmap(QtGui.QPixmap('./test/img1.png')) '

或

' photo = QtWidgets.QGraphicsPixmapItem((QtGui.QPixmap('./test/img1.png'))) '

或者

' photo = QtWidgets.QGraphicsPixmapItem(QPixmap.fromImage(QtGui.QImage('./test/img1.png')))'

### 2

' scene = QtWidgets.QGraphicsScene(self).addItem(phone) '

### 3

' QtWidgets.QGraphicsView.setScene(scene) '

顺序：(QImageQ -->) Pixmap --> QGraphicsPixmapItem --> QGraphicsScene --> QGraphicsView

# QT 四类图片处理方式

Qt provides four classes for handling image data: QImage , QPixmap , QBitmap and QPicture . 

QImage is designed and optimized for I/O, and for direct pixel access and manipulation, while QPixmap is designed and optimized for showing images on screen. 
QBitmap is only a convenience class that inherits QPixmap , ensuring a depth of 1. Finally, the QPicture class is a paint device that records and replays QPainter commands.

Because QImage is a QPaintDevice subclass, QPainter can be used to draw directly onto images. When using QPainter on a QImage , the painting can be performed in another thread than the current GUI thread.

The QImage class supports several image formats described by the Format enum. These include monochrome, 8-bit, 32-bit and alpha-blended images which are available in all versions of Qt 4.x.

QImage provides a collection of functions that can be used to obtain a variety of information about the image. There are also several functions that enables transformation of the image.

QImage objects can be passed around by value since the QImage class uses implicit data sharing . QImage objects can also be streamed and compared.
