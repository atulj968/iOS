# iOS
iOS is a mobile operating system created and developed by Apple Inc. iOS 11.
## What will I learn in this course?
### How to built cool apps.
  - Easy to built even very complex applications.
  - Result lives in your pocket or bagpack.
  - Very easy to distribute your application through the Appstore.
  
### Real-life Object Oriented Programming.
  - The heart of Cocoa Touch is 100% object-oriented.
  - Application of MVC design model.
  - Many computer science concepts applied in a commercial development plateform:
      Database, Graphics, Multimedia, Multithreading, Animation, Networking, and much more...
## Prerequisites
### Prior Coursework
  - Object-Oriented Programming experience mendatory.
  - CS106A&B(or X) reuired & CS107 or CS108 or CS110 also(at minimum)required.
### Parts
  * Core OS 
  
            > OSX Kernel
            > Mach 3.0
            > BSD
            > Sockets
            > Sequrity
            > Power Management
            > Keychain Access
            > Certificates
            > File System
            > Bonjour
    
   * Core Service
    
            > Collections
            > Address Book
            > Networking
            > File Access
            > SQLite
            > Core location
            > Net Service
            > Threading
            > Preference
            > URL Utilities
   * Media
   
            > Core Audio
            > OpenAL
            > Audio Mixing
            > Audio Recording
            > Video Playback
            > JEPG, PNG, TIEF
            > PDF
            > Quartz(2D)
            > Core Animation
            > OpenGLES
            
   * Cocoa Touch
    
            > Multitouch
            > Core Motion
            > View Hierarchy
            > Localization
            > Controls
            > Alerts
            > Web View
            > Map-kit
            > Image Picer
            > Camera
            
    - Cocoa Touch is the UI layer of iOS, where button and the sliders lies.

## Plateform Components
  * Tools - XCode,  Instruments.
  * Language - Swift, Objective-C
  * Frameworks - Foundation, Coredata, UIKit, MapKit etc.
  * Design Strategy - MVC(Model view control)

## Demo
  - Concentration Game
    All this stuff can be very abstract until you see it in action.
    We'll start getting comfortable with Swift4 and XCode 9 by building something right away.
    
  - Topic of Demo
    - Creating a project in XCode9, including building a UI and running in the iOS simulator subclassing in Swift, including how to specify instance variable and methods connecting UI elements to invoke methods in our Swift code print(Outputting to the console using \() notatoin)
    - Connection properties(instance variables) from our Swift code to the UI(Outlet).
    - Accesing iOS documentaion from our code.
    - Automatically doing something everytime a property's value changes.
    - Array
    - Optional
## Let's Create
    1. Open XCode.
    2. Select 'Get Start a new Project'.
    3. Click on iOS.
    4. Select 'Single Line'.
    5. Give Application name.
      - Language :Swift.
      - Select location
    6. Set the active scheme(iPhone X).
    7. Run and See simulator.
    8. Make a new folder 'Supporting File' and drop 'AppDelegate.swift, Assets.cossents, LaunceScreen.storyboard' in it.
    9. Main.storyboard shows UI where you drag and do things, view as iPhone 8 it means it is iPhone8 size screen.
    10. Show the utility bar click on Object-Library.
    11. Catch button and drag it on UI, Change the size & rename(double click)
    12. Click on Attribute inspector and go to view and change the background color of card.
    13. Click the screeen and change the background color from view.
    14. Putting an imoji on card.(but it is too small, so we go to utility bar and change the font size.
    15. Now run and check Simulator.
      - **Simulator** : Look like iPhone, iPad or what we set on Active scheme in XCode and shows how App is working.
    16. Now we see on simulator that if we click on that button it flash but not flips here we need to flip it so....
    17. Now we are going to write a swift code(.swift) to flip card on click-
### Swift Code:
  * import UIKit - UIKit is iOS's framework that has button & sliders etc.
  * class ViewController: UIViewController{} - Here we are going to declaring the class in an Object-Oriented.
  * ViewController - Super Class, here inheriting from UIViewController.This class knows everything about controlling a UI.
  
  import UIKit<br/>
  class ViewController: UIViewController{<br/>
  ...<br/>
  }
  ```
  18. Click on Assitant editor to make both(UI+Code) on same screen.
  ```
  import UIKit<br/>
  class ViewController: UIViewCOntroller{<br/>
  ```
  //hold control key and drag a line from card to code
  //pop-up comes so choose the connection(Action) & name it(touchCard).
  //Argument(Sender).
  //Type: this is type of argument(UIButton).
  //Click connect.
  //After click this is gonna give you a method.
  ```
  @ IBAction func touchCard(_ sender: UIButton)
  ```
  //this is your firstlook at a swift method.
  //func-keyboard of function.
  // *Here is legal to have a funtion outside of class, they are global function.*
  // touchCard is name of method.
  //(_ sender: UIButton) : list of argument, UIButton is type.
  ```
  {<br/>
  flipCard(with Emoji: "👻", on: sender)<br/>
  //print("Agh! A ghost<br/>
  }
  ```
  //run the program and when you click on ghost it will show you on console.
  ```
  func flipCard(withEmoji emoji: string, on button: UIButton)
  ```
  // here I am just gonna have this flipCard method look at the button if it's already the ghost them I'm gonna have it, flip it over to orange with no text if not then we go to put the ghost on it with white background.
  ```
  {<br/>
    if button.currentTitle = emoji{<br/>
      button.setTitle(" ", for:UIControlState.normal(<br/>
      button.background = 🔸<br/>
      }<br/>
     else{<br/>
      button.setTitle(emoji,for:UIControlState.normal)<br/>
      button.background = ▢<br/>
      }<br/>
   }
   ```
   //in 1st line sending message to button asking for current title when you press(.) it shows all mathos & variable.
   // button.setTitle: New button is already here has the ghost on it how I want to give orange or black we give blank string because we want nothing on back side.
   //UIControlState: control taped impass(press option and take courser there and click on it, it will show you documentation) we need a normal control state.
  // set background color type"color.Literal" gives a square and you can select color.
  // In else we just set it to emoji & set backgorund color.
  ```
