# mouse-project-starting
import cv2
cap = cv2.VideoCapture(0)
while(1):
    _, frameinv = cap.read()
    frame = cv2.flip( frameinv, 1)
    hsv = cv2.cvtColor( frame, cv2.COLOR_BGR2HSV)
    cv2.imshow('Frame', hsv)
 k = cv2.waitKey(10) & 0xFF
    if k == 27:
        break
cap.release()
cv2.destroyAllWindows()
