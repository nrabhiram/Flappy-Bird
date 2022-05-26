# Flappy Bird

**Unreal Engine Version**: 4.27

**YouTube Demo**: https://youtu.be/2MppRJZhQ7U

## Development

- To get started with the project, you need to have a version Unreal Engine installed that is greater than or equal to 4.27.
- `git clone https://github.com/nrabhiram/Flappy-Bird.git`

## Navigation

Here's a brief summary of how the content folders are structured within the project.

![Folders](https://user-images.githubusercontent.com/62073792/170465585-25adb314-7a64-46cd-9635-54ec43ee4118.png)

- **Audio** → Sound Cue assets for death, collection of points, and flapping of wings
- **Blueprints** → All of the classes created for the game are stored in this folder. This includes the _Gameplay Framework Classes_, a pipe spawner, backround, foreground, boundaries, camera shake, etc.
- **Levels** → The Game Level is stored in this folder
- **Materials** → Materials background and foreground, both moving and stationary 
- **Sprites** → Sprite assets for the bird, pipes, foreground, and background
- **UI** → Widget blueprints for the Heads-Up Display (HUD), menu options and other UI assets such as the "Game Start" and "Game Over" text.

## Reflections

- **Learned how to use Event Dispatchers** → I used Event Dispatchers in cases where code had to be triggered in multiple Blueprints. Ex. When the bird dies, I call an Event Dispatcher so that the Blueprints that have subscribed to it perform specific actions such as making the background stationary and stopping the pipes from spawning.
- **Used Component Tags to write Overlap logic** → The result of the overlap differs depending on what the bird hit and that is determined by the hit component's tag.
- **Utilized the Game State Class** → I used the Game State class to hold information regarding the current state of the game such as:
  - whether the player has activated the game, i.e. they have clicked the left-mouse button
  - whether the player is dead
  
  These variables were made private, but public getter functions are available.
  