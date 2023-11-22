# Death-Barrier-Tutorials-real
Creating A death Barrier inside of unity

Creating a death barrier and making the game restart is much more similar than people think; however, with this tutorial, it will be a lot easier.

First, you must go inside the hierarchy section and create a 2D sprite like a cube. Once you have made the cube, you must re-size it and change the colour to make it easily visible while creating the death zone. You will also want to move the death zone close to the Player so that you will be able to see if the code works or not. However, you can move it to where you want to after the last thing you will need to add to the sprite is add a box collision 2D and make sure that you turn on is trigger.
![image](https://github.com/RyanJosephMills/Death-Barrier-Tutorial-/assets/146854317/ad356833-892f-494b-bd44-c3fbeeffc1b3)
![image](https://github.com/RyanJosephMills/Death-Barrier-Tutorial-/assets/146854317/838ecb69-2a0d-4fea-803e-8c17996d08a2)

Once you have created the death zone, you must start coding it to kill the Player. So, you must first create a brand new script and call it Kill Player. Then, you can drag and drop it onto the Kill Player sprite and double-click on the code to open up Visual Studio.
![image](https://github.com/RyanJosephMills/Death-Barrier-Tutorial-/assets/146854317/51664df4-81c8-44a5-8586-d1a9d762eb12)


Once inside, at the top of the code, the first thing that you will need to type is using UnityEngine.SceneManagement This is because we use scenes to respawn the character. ![image](https://github.com/RyanJosephMills/Death-Barrier-Tutorial-/assets/146854317/decf8e87-c5e1-473a-aacf-ca897386b301)

Then, just above the void Start, you must create a public variable called int respawn. What this will do is it will appear in Unity, and you will be able to put a number inside, and that will be the scene that the Player will respawn inside.
![image](https://github.com/RyanJosephMills/Death-Barrier-Tutorial-/assets/146854317/0870d908-9bf7-4e33-9713-9301a7c4c75e)
![image](https://github.com/RyanJosephMills/Death-Barrier-Tutorial-/assets/146854317/12112424-ca24-4fea-af3e-3756e64bf690)

The next thing you will need to do is ignore the Start and the Update sections, as we will not need them. Instead, we must create a new variable called OnTriggerEnter2D(Collider2D Collison). When you have that variable, you will need to change collision to other. This is because we want it to work when we collide with it instead of it colliding with us.
![image](https://github.com/RyanJosephMills/Death-Barrier-Tutorial-/assets/146854317/17b8c2f9-d66d-4577-9847-724c00a51d6f)


Once you have changed that, you will then need to create an if statement, and instead of true, you will need to put (other.CompareTag(“Player)). This tells Unity that if something with the tag called Player makes contact with the collision, then do this command, and inside of the if statement, you will need to put SceneManger.LoadScene(Respawn), and this code does if anything with the tag of Player makes contact with this object, it will restart the scene from the beginning.
![image](https://github.com/RyanJosephMills/Death-Barrier-Tutorial-/assets/146854317/bbb7834e-ee89-492e-90be-800975075c04)


So, the final thing you must do is save the code inside Visual Studio, return to Unity, and click on the kill player inside the hierarchy. Then, inside the inspector, ensure the respawn number is the same as the scene you are currently on.
![image](https://github.com/RyanJosephMills/Death-Barrier-Tutorial-/assets/146854317/f6f66cbe-4e8a-473c-b2a3-9d26946f3c0b)

https://github.com/RyanJosephMills/Death-Barrier-Tutorial-/assets/146854317/06e10284-490f-4794-801f-bd2d5d6b50b8
