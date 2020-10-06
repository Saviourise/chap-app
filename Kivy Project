####################################

###                     Importing Starts                       ###

####################################

from kivymd.theming import ThemeManager

from kivymd.app import MDApp

from kivymd.uix.screen import Screen

from kivymd.toast import toast

import sqlite3 as sql

from kivy.uix.image import Image

from kivymd.uix.button import MDRectangleFlatButton, MDFlatButton,MDFloatingActionButtonSpeedDial, MDTextButton, MDIconButton, MDFloatingActionButton, MDRectangleFlatIconButton, MDRaisedButton

from kivy.lang import Builder

from kivy.uix.screenmanager import ScreenManager, Screen

from kivy.uix.boxlayout import BoxLayout

from kivy.properties import ObjectProperty

from kivymd.uix.dialog import MDDialog

from kivy.metrics import dp

from kivymd.uix.picker import MDThemePicker as tp

import time

####################################

###                      Importing Ends                        ###

####################################

####################################

###                   Builder Code Starts                      ###

####################################

##########    Layout Screens    ############

nav = """

MyLayout:

    toolbar: toolbar.__self__

    toolbar2: toolbar2.__self__

    toolbar3: toolbar3.__self__

    nav_drawer: nav_drawer.__self__

    mdc:mdc.__self__

    textb: textb.__self__

    ll: ll.__self__

    pn: pn

    psn: psn

    email: email

    changepass: changepass

    rchangepass: rchangepass

    cpb:cpb

    datecre: datecre

    cb: cb.__self__

    input: input

    password: password

    namesign: namesign

    surname: surname

    username: username

    emailsign: emailsign

    passwordsign: passwordsign

    rpasswordsign: rpasswordsign

    un: un

    scr_mngr: scr_mngr

    user_username: user_username

    user_name: user_name

    orientation: 'vertical'

    ScreenManager:

        id: scr_mngr

        screen1: screen1.__self__

        screen2: screen2

        screen3: screen3.__self__

        screen4: screen4.__self__

        screen5: screen5.__self__

        screen6: screen6.__self__

        screen7: screen7.__self__

        LoginScreen:

            id: screen1

            name: 'screen1'

            toolbar: toolbar.__self__

            input: input

            password: password

            NavigationLayout:

                ScreenManager:

                    Screen:

                        BoxLayout:

                            orientation:"vertical"

                            MDToolbar:

                                id: toolbar

                                specific_text_color: [255/255.0,140/255.0,0,1]

                                #right_action_items: [['format-color-highlight', lambda x: root.theme_color()]]

                                title:"SavieeBase Log In"

                                elevation: 10

                                

                                    

                            MDLabel:

                                    

                                    

                                    

            MDTextField:

                id:input

                mode:"fill"

                fill_color: 0, 0, 0, .4

                color_mode:"custom"

                line_color_focus:  [255/255.0,140/255.0,0,1]

                required: True

                hint_text: "Enter Username"

                helper_text: "Enter a valid username and password"

                helper_text_mode: "on_error"

                icon_right: "account"

                icon_right_color: [255/255.0,180/255.0,0,1]

                pos_hint: {'center_x':0.5, 'center_y':0.7}

                size_hint_x: (0.9)

                size_hint_y: None

                height:20

                                        

                                        

            MDTextField:

                id:password

                mode:"fill"

                fill_color: 0, 0, 0, .4

                color_mode:"custom"

                line_color_focus:  [255/255.0,140/255.0,0,1]

                password:True

                hint_text: "Enter Password"

                helper_text: "Click submit when done"

                helper_text_mode: "on_focus"

                icon_right: "lock"

                icon_right_color: [255/255.0,180/255.0,0,1]

                pos_hint: {'center_x':0.5, 'center_y':0.6}

                size_hint_x: (0.9)

                size_hint_y: None

                height:20

                                        

                                        

            MDCheckbox:

                on_active: root.on_checkbox_active(*args)

                active: False

                size_hint: None, None

                size:"48dp", "48dp"

                pos_hint: {'center_x': .1, 'center_y': .5}

                selected_color: [255/255.0,140/255.0,0,1]

                unselected_color: [.6,.3,.3,1]

                                        

                                        

            MDLabel:

                text: "Show Password"

                pos_hint: {'center_x': .65, 'center_y': .5}

                font_size:25

                color:  [255/255.0,140/255.0,0,1]

                

            MDTextButton:

                text: "Forgot Password"

                pos_hint: {'center_x': .8, 'center_y': .5}

                font_size:25

                on_press: root.fp()

                color:  [255/255.0,140/255.0,0,1]

                                        

                                        

            MDLabel:

                text: "*  Username and Password are case sensitive"

                pos_hint: {'center_x': .58, 'center_y': .45}

                font_size:15

                color:  [255/255.0,140/255.0,0,1]

                    

            MDRaisedButton:

                text:"Log In"

                pos_hint:{'center_x':0.5, 'center_y':0.4}

                on_release: root.show()

                theme_text_color:"Custom"

                text_color:[255/255.0,140/255.0,0,1]

                    

            MDLabel:

                text: "OR"

                pos_hint: {'center_x': .98, 'center_y': .35}

                font_size:25

                color:  [255/255.0,140/255.0,0,1]

                    

            MDRaisedButton:

                text:"Create Account"

                pos_hint:{'center_x':0.5, 'center_y':0.3}

                on_release:root.scr_mngr.current = 'screen2'

                theme_text_color:"Custom"

                text_color:[255/255.0,140/255.0,0,1]

                        

                                     

                            

        SignupScreen:

            name:'screen2'

            id:screen2

            namesign: namesign

            surname: surname

            username: username

            passwordsign: passwordsign

            rpasswordsign: rpasswordsign

            emailsign: emailsign

            

            NavigationLayout:

                ScreenManager:

                    Screen:

                        BoxLayout:

                            orientation:"vertical"

                            MDToolbar:

                                id: toolbar2

                                specific_text_color: [255/255.0,140/255.0,0,1]

                                title:"SavieeBase Sign Up"

                                elevation: 10

                                

                                    

                            MDLabel:

                                    

                                    

                                    

            MDTextField:

                id: namesign

                mode:"fill"

                fill_color: 0, 0, 0, .4

                color_mode:"custom"

                line_color_focus:  [255/255.0,140/255.0,0,1]

                required: True

                hint_text: "Name"

                helper_text: "Enter your name"

                helper_text_mode: "on_error"

                icon_right: "account"

                icon_right_color: [255/255.0,180/255.0,0,1]

                pos_hint: {'center_x':0.5, 'center_y':0.85}

                size_hint_x: (0.9)

                size_hint_y: None

                height:20

                

            MDTextField:

                id: surname

                mode:"fill"

                fill_color: 0, 0, 0, .4

                color_mode:"custom"

                line_color_focus:  [255/255.0,140/255.0,0,1]

                required:True

                hint_text: "Surname"

                helper_text: "Enter your Surname"

                helper_text_mode: "on_error"

                icon_right: "account"

                icon_right_color: [255/255.0,180/255.0,0,1]

                pos_hint: {'center_x':0.5, 'center_y':0.75}

                size_hint_x: (0.9)

                size_hint_y: None

                height:20

                    

            MDTextField:

                id: username

                mode:"fill"

                fill_color: 0, 0, 0, .4

                color_mode:"custom"

                line_color_focus:  [255/255.0,140/255.0,0,1]

                required:True

                hint_text: "Username"

                helper_text: "Choose a Username"

                helper_text_mode: "on_error"

                icon_right: "account"

                icon_right_color: [255/255.0,180/255.0,0,1]

                pos_hint: {'center_x':0.5, 'center_y':0.65}

                size_hint_x: (0.9)

                size_hint_y: None

                height:20

                

            MDTextField:

                id: emailsign

                mode:"fill"

                fill_color: 0, 0, 0, .4

                color_mode:"custom"

                line_color_focus:  [255/255.0,140/255.0,0,1]

                required: True

                hint_text: "Email"

                helper_text: "Enter your email"

                helper_text_mode: "on_error"

                icon_right: "email"

                icon_right_color: [255/255.0,180/255.0,0,1]

                pos_hint: {'center_x':0.5, 'center_y':0.55}

                size_hint_x: (0.9)

                size_hint_y: None

                height:20

                    

            MDTextField:

                id: passwordsign

                mode:"fill"

                fill_color: 0, 0, 0, .4

                color_mode:"custom"

                line_color_focus:  [255/255.0,140/255.0,0,1]

                required:True

                password: True

                hint_text: "Password"

                helper_text: "Choose a password"

                helper_text_mode: "on_error"

                icon_right: "lock"

                icon_right_color: [255/255.0,180/255.0,0,1]

                pos_hint: {'center_x':0.5, 'center_y':0.45}

                size_hint_x: (0.9)

                size_hint_y: None

                height:20

                    

            MDTextField:

                id: rpasswordsign

                mode:"fill"

                fill_color: 0, 0, 0, .4

                color_mode:"custom"

                line_color_focus:  [255/255.0,140/255.0,0,1]

                required:True

                password:True

                hint_text: "Repeat your password"

                helper_text: "Repeat your password"

                helper_text_mode: "on_error"

                icon_right: "lock"

                icon_right_color: [255/255.0,180/255.0,0,1]

                pos_hint: {'center_x':0.5, 'center_y':0.35}

                size_hint_x: (0.9)

                size_hint_y: None

                height:20

                

            MDCheckbox:

                id: cb

                disabled: False

                on_active: root.on_checkbox_actives(*args)

                active: False

                size_hint: None, None

                size:"48dp", "48dp"

                pos_hint: {'center_x': .1, 'center_y': .28}

                selected_color: [255/255.0,140/255.0,0,1]

                unselected_color: [.6,.3,.3,1]

                                        

                                        

            MDLabel:

                text: "Show Password"

                pos_hint: {'center_x': .65, 'center_y': .28}

                font_size:25

                color:  [255/255.0,140/255.0,0,1]

                                        

                                        

            MDLabel:

                text: "*  All input are required"

                pos_hint: {'center_x': .6, 'center_y': .24}

                font_size:25

                color:  [255/255.0,140/255.0,0,1]

                                        

                    

            MDRaisedButton:

                text:"Submit"

                pos_hint:{'center_x':0.5, 'center_y':0.18}  

                on_release:root.submit()     

                theme_text_color:"Custom"

                text_color:[255/255.0,140/255.0,0,1]

                    

            MDLabel:

                text: "OR"

                pos_hint: {'center_x': .98, 'center_y': .13}

                font_size:25

                color:  [255/255.0,140/255.0,0,1]

                    

            MDRaisedButton:

                text:"Login"

                pos_hint:{'center_x':0.5, 'center_y':0.08}

                on_release:root.scr_mngr.current = 'screen1'

                theme_text_color:"Custom"

                text_color:[255/255.0,140/255.0,0,1]

        HomeScreen:

            id: screen3

            name: 'screen3'

            NavigationLayout:

                id:nl

                ScreenManager:

                    Screen:

                        BoxLayout:

                            orientation:"vertical"

                            

                            MDToolbar:

                                id: toolbar3

                                specific_text_color: [255/255.0,140/255.0,0,1]

                                left_action_items: [['menu', lambda x: nav_drawer.toggle_nav_drawer()]]

                                title:"SavieeBase"

                                elevation: 10

                             

                            Widget:

                                                        

                MDNavigationDrawer:

                    id: nav_drawer

                    

                    BoxLayout:

                        id: bl

                        orientation:"vertical"

                        padding: '8dp'

                        spacing: '8dp'

                        

                        AnchorLayout:

                            anchor_x: "center"

                            size_hint_y: (0.3)

                            

                        

                            Image:

                                source: "crop.png"

                    

                        AnchorLayout:

                            anchor_x: "center"

                            size_hint_y: None

                            height:user_username.height

                            

                            MDLabel:

                                id: user_username

                                text: "Admin"

                                font_style: "Subtitle1"

                                font_size:45

                                size_hint_y: None

                                color:  [255/255.0,140/255.0,0,1]

                                height: self.texture_size[1]

                                

                        AnchorLayout:

                            anchor_x: "center"

                            size_hint_y: None

                            height: user_name.height

                            

                            MDLabel:

                                id: user_name

                                text: "Saviour Ise"

                                font_style: "Caption"

                                font_size:25

                                size_hint_y: None

                                color:  [.3, .3, .3, 1]

                                height: self.texture_size[1]

                                

                            

                        ScrollView:

                            id: ll

                            MDList:

                                OneLineIconListItem:

                                    text:"Profile"

                                    on_press: root.proscr()

                                    on_release: nav_drawer.toggle_nav_drawer()

                                    IconLeftWidget:

                                        icon:"account-circle"

                                        on_press: root.proscr()

                                        on_release: nav_drawer.toggle_nav_drawer()

                                        

                                OneLineIconListItem:

                                    text:"Settings"

                                    on_press: root.gtss()

                                    on_release: nav_drawer.toggle_nav_drawer()

                                    IconLeftWidget:

                                        icon:"tools"

                                        on_release: nav_drawer.toggle_nav_drawer()

                                        

                                OneLineIconListItem:

                                    text:"Logout"

                                    on_press: root.logout()

                                    on_release: nav_drawer.toggle_nav_drawer()

                                    IconLeftWidget:

                                        icon:"logout"

                                        on_press: root.logout()

                                        on_release: nav_drawer.toggle_nav_drawer()

                            

        ProfileScreen:

            id:screen4

            name:'screen4'

            MDIconButton:

                icon:"arrow-left"

                user_font_size: "35sp"

                size: "54dp", "54dp"

                pos_hint:{'center_x':0.1, 'center_y':.95}

                theme_text_color: "Custom"

                text_color: [255/255.0,140/255.0,0,1]

                on_press: root.backbtn()

                

            MDCard:

                id:mdc

                orientation: "vertical"

                padding: "8dp"

                size_hint: None, None

                size: "380dp", "700dp"

                pos_hint: {"center_x": .5, "center_y": .5}

        

                MDLabel:

                    text: "Profile"

                    theme_text_color: "Custom"

                    text_color: [255/255.0,140/255.0,0,1]

                    size_hint_y: None

                    font_size:45

                    

        

                MDSeparator:

                    height: "1dp"

                    

                Image:

                    source: "saviee.jpg"

        

                ScrollView:

                    id:ll

                    MDList:

                        TwoLineIconListItem:

                            id: pn

                            text:"Name"

                            secondary_text:""

                            IconLeftWidget:

                                icon:"account-circle"

                                

                        TwoLineIconListItem:

                            id:psn

                            text:"Surname"

                            secondary_text:""

                            IconLeftWidget:

                                icon:"account-circle"

                                

                        TwoLineIconListItem:

                            id: un

                            text:"Username"

                            secondary_text:""

                            IconLeftWidget:

                                icon:"account-circle"

                                

                        TwoLineIconListItem:

                            id: email

                            text:"Email"

                            secondary_text:""

                            IconLeftWidget:

                                icon:"email"

                                

                        TwoLineIconListItem:

                            text:"Profile picture"

                            secondary_text:"Set"

                            IconLeftWidget:

                                icon:"camera-plus"

                                

                        TwoLineIconListItem:

                            id: datecre

                            text:"Date Created"

                            secondary_text:""

                            IconLeftWidget:

                                icon:"calendar-account"

                                

        SettingsScreen:

            id:screen5

            name:"screen5"

            

            NavigationLayout:

                id:nl

                ScreenManager:

                    Screen:

                        BoxLayout:

                            orientation:"vertical"

                            

                            MDToolbar:

                                id: toolbar3

                                specific_text_color: [255/255.0,140/255.0,0,1]

                                left_action_items: [['arrow-left', lambda x: root.backbtn()]]

                                

                                title:"SavieeBase Settings"

                                elevation: 10

                             

                            Widget:

            

            MDLabel:

                text: "Use Mobile Data for app"

                pos_hint: {'center_x': .6, 'center_y': .9}

                font_size:25

                color:  [255/255.0,140/255.0,0,1]

                

            MDSwitch:

                pos_hint: {'center_x': .9, 'center_y': .9}

                active: True

                thumb_color_down: [255/255.0,140/255.0,0,1]

            

            MDLabel:

                text: "Change theme"

                pos_hint: {'center_x': .6, 'center_y': .8}

                font_size:25

                color:  [255/255.0,140/255.0,0,1]

                

            MDIconButton:

                icon:"format-color-highlight"

                on_press: root.theme_color()

                pos_hint: {'center_x': .92, 'center_y': .8}

                user_font_size: "35sp"

                size: "54dp", "54dp"

                theme_text_color: "Custom"

                text_color: [255/255.0,140/255.0,0,1]

                

            MDTextButton:

                id: textb

                text: "Account Settings"

                on_release: root.accset()

                pos_hint: {'center_x': .23, 'center_y': .7}

                font_size:25

                color:  [255/255.0,140/255.0,0,1]

              

                

            MDIconButton:

                icon:"account-arrow-right"

                on_press: root.accset()

                pos_hint: {'center_x': .92, 'center_y': .7}

                user_font_size: "35sp"

                size: "54dp", "54dp"

                theme_text_color: "Custom"

                text_color: [255/255.0,140/255.0,0,1]

                

                

        AccountSettingsScreen:

            id:screen6

            name:"screen6"

                

            MDCard:

                id:mdc

                orientation: "vertical"

                padding: "8dp"

                size_hint: None, None

                size: "380dp", "820dp"

                pos_hint: {"center_x": .5, "center_y": .5}

        

                MDLabel:

                    text: "Account Settings"

                    theme_text_color: "Custom"

                    text_color: [255/255.0,140/255.0,0,1]

                    size_hint_y: None

                    font_size:45

                    

        

                MDSeparator:

                    height: "1dp"

                    

                Image:

                    source: "crop.png"

        

                ScrollView:

                    id:ll

                    MDList:

                        OneLineIconListItem:

                            text:"Change Profile Picture"

                            on_press: root.na()

                            IconLeftWidget:

                                icon:"camera-plus"

                                on_press: root.na()

                                

                        OneLineIconListItem:

                            text:"Change Username"

                            on_press: root.na()

                            IconLeftWidget:

                                icon:"account-circle"

                                on_press: root.na()

                                

                        OneLineIconListItem:

                            text:"Change Password"

                            on_press: root.cps()

                            IconLeftWidget:

                                icon:"lock"

                                on_press: root.cps()

                                

                        OneLineIconListItem:

                            text:"Change Email"

                            on_press: root.na()

                            IconLeftWidget:

                                icon:"email"

                                on_press: root.na()

                                

                        OneLineIconListItem:

                            text:"Delete Account"

                            on_press: root.deleteacc()

                            IconLeftWidget:

                                icon:"delete"

                                on_press: root.deleteacc()

                                

                        OneLineIconListItem:

                            text:"Log Out"

                            on_press: root.logout()

                            IconLeftWidget:

                                icon:"logout"

                                on_press: root.logout()

                                

                        OneLineIconListItem:

                            text:"Back"

                            on_press: root.acc()

                            IconLeftWidget:

                                icon:"arrow-right"

                                on_press: root.acc()

                

        ChangePasswordScreen:

            id:screen7

            name:"screen7"

            NavigationLayout:

                id:nl

                ScreenManager:

                    Screen:

                        BoxLayout:

                            orientation:"vertical"

                            

                            MDToolbar:

                                id: toolbar3

                                specific_text_color: [255/255.0,140/255.0,0,1]

                                left_action_items: [['arrow-left', lambda x: root.bcps()]]

                                #right_action_items: [['lock', lambda x: None]]

                                title:"SavieeBase Change Password"

                                elevation: 10

                             

                            Widget:

                                

            MDTextField:

                id:changepass

                mode:"fill"

                fill_color: 0, 0, 0, .4

                color_mode:"custom"

                line_color_focus:  [255/255.0,140/255.0,0,1]

                password:True

                hint_text: "Enter New Password"

                helper_text: "Click submit when done"

                helper_text_mode: "on_focus"

                icon_right: "lock"

                icon_right_color: [255/255.0,180/255.0,0,1]

                pos_hint: {'center_x':0.5, 'center_y':0.6}

                size_hint_x: (0.9)

                size_hint_y: None

                height:20

                

            MDTextField:

                id:rchangepass

                mode:"fill"

                fill_color: 0, 0, 0, .4

                color_mode:"custom"

                line_color_focus:  [255/255.0,140/255.0,0,1]

                password:True

                hint_text: "Repeat Password"

                helper_text: "Click submit when done"

                helper_text_mode: "on_focus"

                icon_right: "lock"

                icon_right_color: [255/255.0,180/255.0,0,1]

                pos_hint: {'center_x':0.5, 'center_y':0.5}

                size_hint_x: (0.9)

                size_hint_y: None

                height:20

                                        

                                        

            MDCheckbox:

                on_active: root.on_checkbox_activesss(*args)

                active: False

                size_hint: None, None

                size:"48dp", "48dp"

                pos_hint: {'center_x': .1, 'center_y': .4}

                selected_color: [255/255.0,140/255.0,0,1]

                unselected_color: [.6,.3,.3,1]

                                        

                                        

            MDLabel:

                text: "Show Password"

                pos_hint: {'center_x': .65, 'center_y': .4}

                font_size:25

                color:  [255/255.0,140/255.0,0,1]

                

            MDRaisedButton:

                id: cpb

                disabled:False

                text:"Change"

                pos_hint:{'center_x':0.5, 'center_y':0.35}

                on_release: root.cp()

                theme_text_color:"Custom"

                text_color:[255/255.0,140/255.0,0,1]

            

"""

####################################

###                   Builder Code Starts                      ###

####################################

####################################

###              Main Layout Class Starts                 ###

####################################

##########    Layout Class     ##########

class MyLayout(BoxLayout):

    scr_mngr = ObjectProperty(None)

    

    toolbar = ObjectProperty(None)

    

    toolbar3 = ObjectProperty (None)

    

        

    def __init__(self, **kwargs):

        super().__init__(**kwargs)

        

    ## When Settings is clicked ##

    def gtss(self):

        self.scr_mngr.current = 'screen5'

        

    ##When Back Button is clicked ##

    def backbtn(self):

        self.scr_mngr.current = 'screen3'

        

    ##When Back Button is clicked ##

    def bcps(self):

        self.scr_mngr.current = 'screen6'

    

    ## When logout is clicked##

    def logout(self):

        self.nobtn = MDFlatButton(

            text="No",

            on_release=self.close

            )

        self.yesbtn = MDRaisedButton(

            text="Yes",

            on_release=self.yes,

            theme_text_color="Custom",

            text_color=[255/255.0,140/255.0,0,1]

            )

        self.dialog = MDDialog(

                    title="Log Out",

                    text="Are you really sure you want to log out? ",

                    size_hint=(0.9,1),

                    buttons=[self.nobtn, self.yesbtn],

                    

                )

                

        self.dialog.open()

        

        

    def acc(self):

        self.scr_mngr.current = 'screen5'

        

    

    def yes(self, obj):

        self.scr_mngr.current = 'screen1'

        self.dialog.dismiss()

        

    def remacc(self, raun):

        ### Connect to Users Database ##

        con = sql.connect("myapp.db")

        cur = con.cursor()

        cur.execute(""" DELETE from users WHERE username = :username""",{'username':raun})

        con.commit()

        con.close()

        

    ## Delete Account ##

    def deleteacc(self):

        self.btn2 = MDRaisedButton (

            text="Yes",

            on_release=self.delacc,

            theme_text_color="Custom",

            text_color=[255/255.0,140/255.0,0,1]

           

            )

        self.closebtn = MDFlatButton(

            text="No",

            on_release=self.close

            )

        self.dialog = MDDialog(

            title="Delete Account",

            text="Do you really want to delete your account?\nIt can't be retrieved after deleted.",

            size_hint=(0.9,1),

            buttons=[self.closebtn, self.btn2],

            )

        self.dialog.open()

    

    def delacc(self, obj):

        input = self.scr_mngr.screen1.input.text

        self.dialog.dismiss()

        self.remacc(input)

        self.scr_mngr.current = 'screen1'

    

    

    ## Account settings function ##

    def accset(self):

        self.scr_mngr.current = 'screen6'

        

    ## ChangePasswordScreen function ##

    def cps(self):

        self.scr_mngr.current = 'screen7'

        

    def updatepass(self, chpa, chun):

    ### Connect to Users Database ##

        con = sql.connect("myapp.db")

        cur = con.cursor()

        cur.execute(""" UPDATE users SET password = :password WHERE username = :username""",{'username':chun, 'password': chpa})

        con.commit()

        con.close()

   

        

    ## When change button is clicked ##

    def cp(self):

        input = self.scr_mngr.screen1.input.text

        if self.changepass.text != "" and self.rchangepass.text!= "":

            if self.changepass.text == self.rchangepass.text:

                if len(self.changepass.text) >= 6:

                   self.updatepass(self.changepass.text, input)

                   self.show_toast('Password changed successfully')

                   self.changepass.text = ""

                   self.rchangepass.text = ""

                   self.scr_mngr.current = 'screen6'

                else:

                    self.show_toast("Passwords must contain more than 6 characters")

            else:

                self.show_toast("Password and Repeat password must be the same")

        else:

            self.show_toast("Please fill all input")

        

       

        

    ## Change Password Show Password ##

    def on_checkbox_activesss(self, checkbox, value):

        if value:

            self.changepass.password= False

            self.rchangepass.password= False

        else:

            self.changepass.password= True

            self.rchangepass.password= True

        

    

    ####   Button to create account screen.  ####

    def btn(self, obj):

        self.scr_mngr.current = 'screen2'

        self.dialog.dismiss()

        self.password.text = ""

        

    

    ##########    Toast Function    ##########

    def show_toast(self, ti):

        '''Displays a toast on the screen.'''

        

        toast(ti)

        

    ## Show password When checkbox is clicked ##

    def on_checkbox_active(self, checkbox, value):

        if value:

            self.password.password= False

        else:

            self.password.password= True

            

    ## Show password When checkbox is clicked ##

    def on_checkbox_actives(self, checkbox, value):

        if value:

            try:

                self.passwordsign.password= False

                self.rpasswordsign.password= False

            except:

                self.cb.disabled= True

        else:

            try:

                self.passwordsign.password= True

                self.rpasswordsign.password= True

            except:

                self.cb.disabled= True

        

        

    ## Theme picker ##

    def theme_color(self):

        #pass

        self.theme_dialog = tp()

        self.theme_dialog.open()

    

    ## Function for functions that are not available #

    def na(self):

        self.show_toast("Function is not available at the moment")

    

    ### Create Database For Storing User Data ###

    try:

        con = sql.connect('myapp.db')

        cur = con.cursor()

        cur.execute(""" CREATE TABLE users(

        name text,

        surname text,

        username text,

        email blob,

        password text,

        year integer,

        month integer,

        day integer)""")

        con.commit()

        con.close()

        print("Table Created Successfully")

    except:

        print('Table exists')

        cur.execute("SELECT * FROM users")

        print(cur.fetchall())

            

        

            

    

    ## Function for when log in button is clicked ##

    def show(self):

        

        ## Get User Login Username and password ##

        

        ## Get username inputted ##

        input = self.scr_mngr.screen1.input.text

        

        ## Get password inputted ##

        password= self.scr_mngr.screen1.password.text

        

        ### Connect to Users Database ##

        con = sql.connect("myapp.db")

        cur = con.cursor()

        cur.execute("SELECT * FROM users")

        users = cur.fetchall()

        

         

       ## Loop through the users database table ##

        try:

            t = 0

            while t>=0:

                #print(t)

                yy = t

                uu = users[t][2]

                if uu == input:

                    self.user= uu

                    break

                t+=1

            y = yy

            self.user_password = ""

            while y==yy:

                #print(y)

                up = users[y][4]

                nn = users[y][0]

                ss = users[y][1]

                eee = users[y][3]

                year = users[y][5]

                month = users[y][6]

                day = users[y][7]

                if up == password:

                    self.user_password=up

                    self.user_nname=nn

                    self.user_surname=ss

                    self.year = year

                    self.month = month

                    self.day = day

                    eeee = eee

                    break

                y+=1

            

        except:

            self.user = ""

            self.user_password=""

                

            

        ## Validate login details by comparing user                     input with data in the users table ##

        

        ## Check that all details are not empty ##

        if (self.user == "" or input == "") and (password == "" or self.user_password == ""):

            cs = "Please input a valid username or password"

            self.password.text = ""

            self.input.text = ""

            self.show_toast(cs)

            

        ## Empty Password ## 

        elif input == self.user and password =="":

            self.show_toast("Password cannot be left empty")

            

         ## Incorrect password ##

        elif input == self.user and (password== "" or password!=self.user_password):

            self.show_toast("Password is incorrect")

            self.password.text = ""

            

        ## Compare login details with data in the                         users database successfully  ##

        elif input == self.user and password == self.user_password:

            ttt = "User " + self.user + " Logged in successfully"

            ye = self.year

            mo = self.month

            da = self.day

            if mo==1:

                mon="Jan"

            elif mo ==2:

                mon ="Feb"

            elif mo ==3:

                mon ="Mar"

            elif mo ==4:

                mon ="Apr"

            elif mo ==5:

                mon ="May"

            elif mo ==6:

                mon ="Jun"

            elif mo ==7:

                mon ="Jul"

            elif mo ==8:

               mon ="Aug"

            elif mo ==9:

                mon ="Sep"

            elif mo ==10:

                mon ="Oct"

            elif mo ==11:

                mon ="Nov"

            elif mo ==12:

                mon ="Dec"

                

            created_date = (str(da) + " " + mon + " " + str(ye))

            cd = created_date

            print(cd)

            self.datecre.secondary_text=(cd)

            self.email.secondary_text = (eeee)

            self.show_toast(ttt)

            self.scr_mngr.current = 'screen3'

            self.user_username.text = self.user

            self.user_name.text = self.user_nname + " " + self.user_surname

            self.pn.secondary_text = self.user_nname

            self.psn.secondary_text = self.user_surname

            self.un.secondary_text = self.user

            self.password.text = ""

       

       ## User does not exist ##

        else:

            cs = "User " + input + " does not exist"

            self.password.text = ""

            self.input.text = ""

        

            self.btn2 = MDRaisedButton (

            text="Create Account",

            on_release=self.btn,

            theme_text_color="Custom",

            text_color=[255/255.0,140/255.0,0,1]

            )

            self.closebtn = MDFlatButton(

            text="Close",

            on_release=self.close

            )

            self.dialog = MDDialog(

            title="User Confirmation",

            text=cs,

            size_hint=(0.9,1),

            buttons=[self.closebtn, self.btn2],

            

            )

            

            self.dialog.open()

#        print(input)

    

    

    ## Function for forgot password button

    def fp(self):

        input = self.scr_mngr.screen1.input.text

        

        ### Connect to Users Database ##

        con = sql.connect("myapp.db")

        cur = con.cursor()

        cur.execute("SELECT * FROM users")

        users = cur.fetchall()

        

         

       ## Loop through the users database table ##

        try:

            t = 0

            while t>=0:

                #print(t)

                yy = t

                uu = users[t][2]

                if uu == input:

                    self.user= uu

                    break

                t+=1

            y = yy

            user_password = ""

            while y==yy:

                #print(y)

                up = users[y][4]

                year = users[y][5]

                month = users[y][6]

                day = users[y][7]

                if up != "":

                    user_password=up

                    self.year = year

                    self.month = month

                    self.day = day

                    break

                y+=1

            

        except:

            self.user = ""

            self.user_password=""

        

        

        ## Compare username with that in the database to fetch out the password ##

        if input==self.user and input != "":

            self.closebtn = MDFlatButton(

            text="Close",

            on_release=self.close

            )

            self.dialog = MDDialog(

                    title="Forgot Password",

                    text="Password for " + self.user + " is " +user_password,

                    size_hint=(0.9,1),

                    buttons=[self.closebtn],

                    

                )

            

            self.password.text = user_password

            self.dialog.open()

        

        ## User does not exist ##

        elif input!=self.user and input!="":

            self.btn2 = MDRaisedButton (

            text="Create Account",

            on_release=self.btn,

            theme_text_color="Custom",

            text_color=[255/255.0,140/255.0,0,1]

           

            )

            self.closebtn = MDFlatButton(

            text="Close",

            on_release=self.close

            )

            self.dialog = MDDialog(

            title="Forgot Password",

            text="Could not find user "+input,

            size_hint=(0.9,1),

            buttons=[self.closebtn, self.btn2],

            )

            try:

                self.password.text = ""

                self.input.text = ""

            except:

                pass

                

            self.dialog.open()

            

        ## Empty value or data ##

        elif input == "" or self.user == "":

            self.show_toast("Please Input a valid username")

            try:

                self.password.text = ""

                self.input.text = ""

            except:

                pass

    

    

    ### Function for close button ##

    def close(self,obj):

        self.dialog.dismiss()

       

   

        

        

    ### Function for creating account button ##

    def submit(self):

        

        

        ## Get user create account input ##

        

        ## User's Name ##

        namesign = self.scr_mngr.screen2.namesign.text

        

        ## User's Surname ##

        surname = self.scr_mngr.screen2.surname.text

        

        ## User's Password ##

        self.passwordsign = self.scr_mngr.screen2.passwordsign.text

        

        ## User's Username

        self.username = self.scr_mngr.screen2.username.text

        

        ## Users Email

        emailsign = self.scr_mngr.screen2.emailsign.text

        

        ## User's Repeat password ##

        rpasswordsign = self.scr_mngr.screen2.rpasswordsign.text

        

        ## Validate create account details  ##

        

        ## Check that no input is empty ##

        if namesign != "" and surname!="" and self.username!="" and self.passwordsign!="" and rpasswordsign!="" and emailsign!="":

            

            ## check that password and repeat password are the same ##

            if self.passwordsign == rpasswordsign:

                

                ## check that username and password are not the same ##

                if self.username==self.passwordsign:

                    self.show_toast("Username and Password cannot be the same")

                    try:

                        self.username.text = ""

                    except:

                        pass

                

                ## check that the length of the password is up to six characters or more ##

                elif len(self.passwordsign) < 6:

                    self.show_toast("Password must contain more than 6 characters")

                    try:

                        self.passwordsign.text = ""

                        self.rpasswordsign.text = ""

                    except:

                        pass

                        

                elif "@" not in emailsign or ".com" not in emailsign:

                    self.show_toast("Please enter a valid email")

                    

                 ## Account created successfully ##

                else:

                    self.show_toast("Account Created Successfully")

                    timestr = time.strftime("%Y")

                    ttimestr = time.strftime("%m")

                    tttimestr = time.strftime("%d")

                    print(timestr+ttimestr+tttimestr)

                    

                    

                    try:

                        self.namesign.text = ""

                        self.surname.text = ""

                        self.username.text = ""

                        self.passwordsign.text = ""

                        self.rpasswordsign.text = ""

                    except:

                        pass

                        

                    self.scr_mngr.current = 'screen1'

                    

                    ## Add create account details to users database table after validation is successful ##

                    con = sql.connect("myapp.db")

                    cur = con.cursor()

                    cur.execute(""" INSERT INTO users (name,surname,username,email,password,year,month,day) VALUES (?, ?, ?, ?, ?, ?, ?, ?)""", (namesign, surname, self.username, emailsign, self.passwordsign, timestr, ttimestr, tttimestr))

                    con.commit()

                    con.close()

                    

            ## Password and Repeat password are the same ##

            else:

                self.show_toast("Password and Repeat password must be the same")

                try:

                    self.rpasswordsign.text = ""

                except:

                    pass

                

        ## one or more input is empty ##

        else:

            self.show_toast("Please fill all input")

            try:

                self.namesign.text = ""

                self.surname.text = ""

                self.username.text = ""

                self.passwordsign.text = ""

                self.rpasswordsign.text = ""

            except:

                pass

            

    ## When profile screen is clicked ##

    def proscr(self):

        self.scr_mngr.current = 'screen4'

            

            

####################################

###               Main Layout Class Ends                  ###

####################################

####################################

###       Adding all Screen Together Starts         ###

####################################

## create Login Screen Class in MyLayout ##

class LoginScreen(Screen):

    pass

### Create Account screen class in MyLayout ##

class SignupScreen(Screen):

    pass

    

### Home screen class in MyLayout ##

class HomeScreen(Screen):

    pass

    

### Profile screen class in MyLayout ##

class ProfileScreen(Screen):

    pass

    

### Settings screen class in MyLayout ##

class SettingsScreen(Screen):

    pass

    

### Account Settings screen class in MyLayout ##

class AccountSettingsScreen(Screen):

    pass

    

### ChangePassword screen class in MyLayout ##

class ChangePasswordScreen(Screen):

    pass

    

## Create the screen manager ##

sm = ScreenManager()

sm.add_widget(LoginScreen(name='screen1'))

sm.add_widget(SignupScreen(name='screen2'))

sm.add_widget(HomeScreen(name='screen3'))

sm.add_widget(ProfileScreen(name='screen4'))

sm.add_widget(SettingsScreen(name='screen5'))

sm.add_widget(AccountSettingsScreen(name='screen6'))

sm.add_widget(ChangePasswordScreen(name='screen7'))

    

####################################

###        Adding all Screen Together Ends          ###

####################################

####################################

###                Main App Class Starts                  ###

####################################

 

##########    Main App Class   ##########

class DemoApp(MDApp):

    

    

    

            

    ##########   Main App Function  ##########

    def build(self):

            

        ### Set the theme color of the app ##

        self.theme_cls.primary_palette = "BlueGray"

            

        self.theme_cls.primary_hue = "A100"

            

        self.theme_cls.theme_style = 'Dark'

            

        

        ##########  Build all screens   ##########

        screen = Builder.load_string(nav)

        

        ### Return built screens ##

        return screen

            

            

    

    

    ### Close button function ##

    def close(self,obj):

        self.dialog.dismiss()

        

####################################

###                  Main App Class Ends                   ###

####################################

            

      

      

##########    Run the app    ##########

if __name__ == '__main__':

    DemoApp().run()
