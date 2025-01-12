# Play Button Tutorial
### In this tutorial, we'll be creating a simple Play Button for your game

> [!IMPORTANT]
> You will need any version of Unity and VisualStudio released within the last 5 years
> 
> This tutorial is made for a 3D Project
> 
> This tutorial also requires 2 Scenes; one of your game, another for the Main Menu, which should be empty

<img width="742" alt="image" src="https://github.com/user-attachments/assets/bae7a596-64b7-4a23-939e-13fe0887610f" />

> Your project should look something like this, with your main menu scene open


### Firstly, we need to create the actual Main Menu UI

1. Right click in the `Heirarchy` -> `UI` -> `Canvas`

![image](https://github.com/user-attachments/assets/7d1cba15-d288-4ed2-9190-c1d000267f8f)

2. Whilst clicked on canvas, you should see its settings in the `Inspector` window. By default, the `Render Mode` is set to 'Screen Space - Overlay'. Change it to 'Screen Space - Camera'.

![image](https://github.com/user-attachments/assets/651a5d43-e0c2-4388-b517-224af1b5ce5b)

3. Next, click your `Main Camera` in `Heirarchy` and drag it to the `Render Camera`.

<img width="362" alt="image" src="https://github.com/user-attachments/assets/111ec4ac-5fdc-4960-ad89-087d5c2705f1" />

4. To add the button to the scene, right click `Canvas` -> `UI` -> `Button`.

![image](https://github.com/user-attachments/assets/604660b8-9e6f-42b2-87b4-779f0464f0fe)

> You can adjust and scale it up to your preferred size in the `Rect Transform` tab. To change the Text, click the drop down arrow next to the 'Button' gameObject.


### Next, we need to make the code for the Play Button

1. Right Click in the `Assets` window, -> `Create` -> `C# Script` and name the script 'MainMenu'. Double click to open in VisualStudio.

![image](https://github.com/user-attachments/assets/2a56b21c-0301-4114-82e4-9d7e5ff7a91f)

<img width="726" alt="image" src="https://github.com/user-attachments/assets/fd45f3f6-4cd2-41bf-98c2-fd5ef83f71fd" />

> Lines 7 - 17 can be deleted, since we won't be using them

2. Because the script will be transferring the player from one scene to another, you'll need to add a new library at the top. on **Line 4**, add  `using UnityEngine.SceneManagement`

3. On **Line 8**, type in the following function:

  ` public void PlayButton()
    {
        SceneManager.LoadScene("Game");
    }`

> [!NOTE]
> In the quotations, you must put the name of your game scene (in this case, the name of the scene is "Game"). Ensure the spelling is correct.

![image](https://github.com/user-attachments/assets/cfdedfb3-5601-407b-bd4e-9c2a7fe385e9)

> Your script should look something like this. Press Ctrl + S to save and return to Unity.


### Lastly, we just need to apply the code to the button

1. In the top left, click `File` and open `Build Settings...`. Drag your two scenes into the allocated window. Then close the window.

<img width="841" alt="image" src="https://github.com/user-attachments/assets/b7ed3846-a4c9-4cb0-b4cd-d7a32b6b7c5d" />

2. Drag your MainMenu script onto your Canvas in `Heirarchy`.
  
3. Now click on the 'Button' gameObject and scroll down until you see the `On Click ()` tab. Click the + icon and drag the canvas where it says `None (Object)`.
> Right click in the Project window and refresh, just to make sure the new script shows up in the functions tab.

4. Click the `No Function` tab -> `Main Menu` -> `Play Button()`.

![image](https://github.com/user-attachments/assets/5cc3b9f4-d290-48b4-9735-aed9064f4212)

### And just like that, you now have a fully functional Play Button!
