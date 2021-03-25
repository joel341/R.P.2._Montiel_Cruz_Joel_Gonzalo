# R.P.2._Montiel_Cruz_Joel_Gonzalo
 codigos en tu portafolio realizados en los ejemplos del material Programacion avanzada.

#ejemplo 1 import wx

app = wx.App(clearSigInt=True) # clearSigInt to allow terminating the program by CTRL+C frame = wx.Frame(parent=None, title="") ## main window object panel = wx.Panel(parent=frame) text = wx.StaticText(parent=panel, label="Hello, from wxPython!!", pos = (40,50)) frame.Show() app.MainLoop()
![image](https://user-images.githubusercontent.com/79875834/112516220-ab935800-8d5c-11eb-9252-2e9e1dc994f1.png)
