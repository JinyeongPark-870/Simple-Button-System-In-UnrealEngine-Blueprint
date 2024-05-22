## Simple-Button-System-In-UnrealEngine-Blueprint
Making an Blueprint Actor that functions as a button with Event-Dispatcher of Unreal Engine. <br>
[Event Dispatcher](https://docs.unrealengine.com/4.27/ko/ProgrammingAndScripting/Blueprints/UserGuide/EventDispatcher/) <br>

Make and call event dispatcher in the event you want to use as the button click function. <br>
> In my case, I used static mesh overlap and click event to call event dispatcher. <br>
<img src = "https://github.com/JinyeongPark-870/Simple-Button-System-In-UnrealEngine-Blueprint/assets/4387404/c20c4ada-c204-4dcb-996a-42791c273e72" width = "90%" height = "90%"> <br>

#

After that, go to the event graph screen of another Actor(for example, i used GameModeBase Blueprint) managing the button system. <br>
Spawn an actor according to the flow of the button system in the event graph. <br>
Create the first button actor to start, and bind event(spawning next button) to be called to the event dispatcher for that button. <br>
[Event Dispatcher Binding/Unbinding](https://docs.unrealengine.com/4.27/ko/ProgrammingAndScripting/Blueprints/UserGuide/EventDispatcher/BindingAndUnbinding/) <br>
When the event is called, it creates a button(or buttons) that spawns next button when it clicked(hit, overlaped, etc), and bind the event for the next action to the event dispatcher of the spawned button. <br>
This repeated structure allows you to complete the button system. <br>
In my example, I destroyed Actor when the next button spawns. When buttons are more than two, I made actor array and managed them. <br>
In summary, make button actor with event dispatcher calling event. In another actor like GameModeBase, spawn that actor and bind event to event dispatcher which spawns next button actors. Make spawned buttons do same action. <br>





링크
[제목](주소)

이미지
<img src = "" width = "50%" height = "50%">
