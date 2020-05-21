# PyQt5

## QGraphicsView 图片显示逻辑

### 1

'photo = QtWidgets.QGraphicsPixmapItem().setPixmap(QtGui.QPixmap('./test/img1.png'))'

或

'photo = QtWidgets.QGraphicsPixmapItem((QtGui.QPixmap('./test/img1.png')))'

###2

'scene = QtWidgets.QGraphicsScene(self).addItem(phone)'

### 3

'QtWidgets.QGraphicsView.setScene(scene)'

顺序：QPixmap --> QGraphicsPixmapItem --> QGraphicsScene --> QGraphicsView
