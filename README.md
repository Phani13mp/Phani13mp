from tkiner import*
import phonenumbers
from phonenumbers import carrier
from phonenumbers import geocoder
from opencage.geocoder import opencagecode
import folium
import webbrowser

root=TK()
root.title("phone number tracker")
root.geometry("385*594+300+200")
root.resizable(flase,flase)
root.comfigure(bg='#968FFF')
key="d2b3af88e38b4b5bb6e04f77a89e39f3"

1 usage
def track():
    enter_nb=entry.get()
    
