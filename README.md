# Unity-Dialogue-System
A Dialogue System for Unity.
To set up, copy the Dialogue folder into you project. 
Create dialogue conversation objects and dialogue line objects by right clicking in the project window, and navigating to 'Dialogue Objects'. You can drag and drop the line objects into the conversation objects to create a conversation.
Once your conversations are finished, in your scene create a dialogue manager object and attach the three components: an Audio Source, 'Manager Script', and 'Dialogue Script'. The scripts will need some references to objects.

Manager Script:
  - 'D Sctipt' takes the Dialogue Script component attached to the dialogue manager object.
  - 'Player' takes the controlled player in the scene.
  - NPCs takes the conversable NPCs in the scene.
  - 'Conversations' takes the conversation objects you have created for your NPCs. 
  - Make sure that you conversations and NPCs are in the correct order such that the NPC in element 0 will speak the conversation in element 0, the NPC in element 1 will speak the conversation in element 1, and so forth.
  
Dialogue Script:
  - 'Manager Script' takes the manager script attached to the dialogue manager object.
  - 'Player' takes the controlled player in the scene.
  - 'Dialogue UI' takes the GameObject which parents all the UI elements specific to dialogue. Make sure it has an alpha canvas attached to it.
  - 'Dialogue text' takes the Text Mesh Pro object which will present all of the speech text.
  - 'Dialogue name' takes the Text Mesh Pro object which will present the name of the person currently talking.
  - 'Dialogue portrait' takes the image which will display a portrait of the crrent speaker.
  - 'Fade duration' is a float which determines how fast the Dialogue UI will fade in to 1 and out from 1.
  - 'Continue SFX' takes the audio source attahced to the manager object which plays when you initiate or continue a conversation with an NPC.

The last thing to do is to decide which conversation should be played, and when. Do this in the manager script. I use trigger box colliders attached to the NPCs to find out which NPC the player is close to.

If someone stumbles across this and would like some help setting it up, post so on the issues page.
