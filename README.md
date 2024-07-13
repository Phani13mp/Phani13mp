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
    number=phonenumbers.parse(enter_nb)
    location=geocoder.description_for_number(number,'en')
    country.config(text=location)
    service=carrier. name_for_number(number,'en)
    sim.config(text=service)
    query= str(location)
    results= opencagegeocode(key).geocode(query)
    lat=results[0]['geometry']['lat']
    lng=result[0]['geometry']['lng']
    mymap=folium.map(location=[lat,lng],zoom_start=9)
    folium.marker([lat,lng],popup=location).add_to(mymap)
    mymap.save("mylocation.html")
    1 usage
    def open_map():
    webbrowser.open("mylocation.html")
    logo=photo image(file="logo.png")
    label(root,image=logo,bg="#96BFF").place(x=135,y=40)
    search=photo image(file="search.png")
    Label(root,image=search,bg="#96BFF").place(x=14,y=244)
    heading=label (root,text="tracknumber",
                font='arial 20 bold',fg="#39281E",
                bg="#96BFF")
    heading.place(x=90,y=190)
    entry=stringvar()
    enter_nb=entry(root,textvariable=entry,width=17,justify='center',bd=0,font='arial20',bg="#2c3541",fg="white")
    enter_nb.place(x=54,y=258)
    search_botton=photoimage(file='search_icon.png')
    btn=button(root,image=search_button,curson='hand2'activebackground='#ED8051')
    btn.place(x=155,y=308)
    country=label(root,text="country",bg='#96BFF',fg='black',font='arial 14 bold")
    country.place(x=55,y=370)
    sim=label(root,text="SIM",bg='96BFFF',fg='black',font='arial 14 bold')
    open_map_btn.place(x=125,y=430)
    insta_page=label(root,text="@pythonagham",bg='#96BFF',fg='black',font='arial 10 bold italic')
    insta.page.place(x=135,y=550)
    root.mainloop()
    
    
