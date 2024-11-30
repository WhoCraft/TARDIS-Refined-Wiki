# Performance Mods

Ah yes, performance mods! We are all guilty of using them!

Now, this is a difficult one to fix, as there is a number of tradeoffs that happen when playing with Performance Mods, one of which is that it drastically changes how the game renders things or how logic is handled!

This leads to an array of problems, sadly we can't fix these problems without actively fighting the reason you installed these mods! 

So instead of talking about how we made it compatible, we will cover some things you may run into!


## Shaders leading to full bright consoles and shells

Follow these steps to integrate Tardis Refined with Complementary Shaders:

1. **Locate the Shaders Folder**
    - Open the folder for Shaders in your Minecraft installation directory.

2. **Open the `shaders` Directory**
    - Inside the shader pack, find and open the `shaders` directory.

3. **Find the `block.properties` File**
    - Look for a file named `block.properties` (or something similar).

4. **Edit the `block.properties` File**
    - Open the `block.properties` file using a suitable text editor (e.g., Notepad++ or VS Code).

5. **Search for "chest"**
    - Locate the section of the file that references regular and trapped chests.

6. **Add Tardis Refined Entry**
    - Add the following line to the same section, ensuring the format matches the existing entries:
      ```plaintext
      tardis_refined:tardis_console
      ```

7. **Save and Test**
    - Save the changes to the file and test the shaders in-game to ensure the Tardis Console appears as intended.


``Note``
: Every Shader is different, we cannot say if this will fix your issue for sure or if the Shader has the files we mention :(
