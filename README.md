code = """
from kivy.app import App
from kivy.uix.boxlayout import BoxLayout
from kivy.uix.button import Button
from kivy.uix.label import Label
import os

class PentestApp(BoxLayout):
    def __init__(self, **kwargs):
        super().__init__(orientation='vertical', **kwargs)
        self.add_widget(Label(text="أداة اختبار الاختراق التجريبية", font_size='20sp'))
        
        btn_qr = Button(text="إنشاء كود ملغم (تجريبي)")
        btn_qr.bind(on_press=self.msg)
        self.add_widget(btn_qr)

    def msg(self, instance):
        print("Action Triggered")

class MyApp(App):
    def build(self):
        return PentestApp()

if __name__ == '__main__':
    MyApp().run()
"""
with open('main.py', 'w') as f:
    f.write(code)
