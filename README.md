# R.P.2._Montiel_Cruz_Joel_Gonzalo
 codigos en tu portafolio realizados en los ejemplos del material Programacion avanzada.

#ejemplo 1 import wx

app = wx.App(clearSigInt=True) # clearSigInt to allow terminating the program by CTRL+C frame = wx.Frame(parent=None, title="") ## main window object panel = wx.Panel(parent=frame) text = wx.StaticText(parent=panel, label="Hello, from wxPython!!", pos = (40,50)) frame.Show() app.MainLoop()
![image](https://user-images.githubusercontent.com/79875834/112516220-ab935800-8d5c-11eb-9252-2e9e1dc994f1.png)

#ejemplo 2 import wx import webbrowser

class MyApp(wx.App): def init(self): super().init(clearSigInt=True)

    # init frame
    self.InitFrame()

def InitFrame(self):
    frame = MyFrame(parent=None, title="Basic Frame", pos=(100, 100))
    frame.Show(True)
class MyFrame(wx.Frame): # subclass of wx.Window; Frame is a top level window # A frame is a window whose size and position can (usually) be changed by the user. # Usually represents the first/main window a user will see def init(self, parent, title, pos=pos): super().init(parent=parent, title=title, pos=pos)

def OnInit(self):
    panel = MyPanel(parent=self)
    ![image](https://user-images.githubusercontent.com/79875834/112516659-1d6ba180-8d5d-11eb-90d8-6b10e291a316.png)

#ejemplo 3 import wx import webbrowser

class MyApp(wx.App): def init(self): super().init(clearSigInt=True)

    # init frame
    self.InitFrame()

def InitFrame(self):
    frame = MyFrame(parent=None, title="my button app", pos = (100, 100))
    frame.Show()
class MyFrame(wx.Frame): # subclass of wx.Window; Frame is a top level window # A frame is a window whose size and position can (usually) be changed by the user. # Usually represents the first/main window a user will see def init(self, parent, title, pos): super().init(parent=parent, title=title, pos=pos) self.OnInit()

def OnInit(self):
    panel = MyPanel(parent=self)
class MyPanel(wx.Panel): # A panel is a window on which controls are placed. (e.g. buttons and text boxes) # wx.Panel class is usually put inside a wxFrame object. This class is also inherited from wxWindow class. def init(self,parent): super().init(parent=parent)

    # add a hello message to the panel
    welcomeText = wx.StaticText(self, label="To learn wxPython, click the link below!", pos=(20,20))

    # add a button to bring up the dialog box
    button = wx.Button(parent=self, label='Click Here!', pos = (20, 120))
    button.Bind(wx.EVT_BUTTON, self.onSubmit) # bind action to button


def onSubmit(self, event):
    # stuff for the submit button to do
    webbrowser.open('https://wxpython.org/Phoenix/docs/html/index.html')
if name == "main": app = MyApp() app.MainLoop() image image
