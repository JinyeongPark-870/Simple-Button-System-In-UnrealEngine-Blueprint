## Simple-Button-System-In-UnrealEngine-Blueprint
Making an Blueprint Actor that functions as a button with Event-Dispatcher of Unreal Engine. <br>
[Event Dispatcher](https://docs.unrealengine.com/4.27/ko/ProgrammingAndScripting/Blueprints/UserGuide/EventDispatcher/) <br>

> Example Button System Image <br>
<img src = "https://github.com/JinyeongPark-870/Simple-Button-System-In-UnrealEngine-Blueprint/assets/4387404/8d55b8c5-1fe3-4559-844f-84bb8aeec18f" width = "30%" height = "30%"> <br>

#

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
<img src = "https://github.com/JinyeongPark-870/Simple-Button-System-In-UnrealEngine-Blueprint/assets/4387404/0dac4473-93cc-43ef-9dd0-a41b01ac2925" width = "90%" height = "90%"> <br>
<img src = "https://github.com/JinyeongPark-870/Simple-Button-System-In-UnrealEngine-Blueprint/assets/4387404/ff71c11f-d3b2-4e2b-abd6-d2336f57897d" width = "90%" height = "90%"> <br>
#

In my example, I destroyed Actor when the next button spawns. When buttons are more than two, I made actor array and managed them. <br>
In summary, make button actor with event dispatcher calling event. In another actor like GameModeBase, spawn that actor and bind event to event dispatcher which spawns next button actors. Make spawned buttons do same action. <br>
> This is my button actor test with my other project : [How to use Kinect V2 sensor data in UnrealEngine 5](https://github.com/JinyeongPark-870/How-to-use-Kinect-V2-sensor-data-in-UnrealEngine-5) <br>
<img src = "https://github.com/JinyeongPark-870/Simple-Button-System-In-UnrealEngine-Blueprint/assets/4387404/825632d7-1a2b-4394-9734-e9cc8383fe65" width = "50%" height = "50%"> <br>
#


<!--
링크
[제목](주소)

이미지
<img src = "" width = "50%" height = "50%">
-->
