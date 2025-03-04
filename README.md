# Guilty Gear Xrd x SAMMI

A Bridge Extension for [SAMMI](https://sammi.solutions). Take interactions in game and turn them into stream gimmicks!

## Extension Function

This extension allows you to receive data from [ggxrd-mod](https://github.com/super-continent/ggxrd-mod) in the form of Extension Triggers inside SAMMI. A collection of example buttons have been provided with some experimental functionality to get you started.

![image](https://github.com/user-attachments/assets/c9cea94d-96bb-44ee-b8aa-9d4483e670a4)

## Quick Start Guide

Step 1: Download [SAMMI](https://sammi.solutions).

Step 2: Follow the various [SAMMI Onboarding Tutorials](https://sammi.solutions/docs/getting-started/step-by-step).

Step 3: Install Guilty Gear Xrd x SAMMI as a [SAMMI Bridge](https://sammi.solutions/docs/bridge) Extension.

Step 4: Boot up Guilty Gear Xrd while SAMMI and SAMMI Bridge are open to automatically connect.

Step 5: Make use of the various Extension Triggers generated by Xrd to drive stream gimmicks!

Step 6 (Optional): Copy the text found in the Example Deck text file to your clipboard, then import it to Sammi via the Paste Deck command. 

## Using the Mod

### Important Notes

#### >>> Run Bridge in a regular browser instead of the embedded OBS dock for better performance.

Run SAMMI at >90FPS to stop button events from backing up. It's a SAMMI thing. This can affect commands like Motion, so if you need to animate things in OBS, I recommend the OBS Move plug-in.
![image](https://github.com/user-attachments/assets/cf509d26-069f-4774-a1f2-543fade5d45a)

### Accessing Events via Extension Triggers

The following Extension Triggers are available for use. Add them to buttons via a button's Trigger menu. They all contain extremely relevant data within that can be accessed via the `Trigger Pull Data` command.

![image](https://github.com/user-attachments/assets/d7188aa0-a8bd-4deb-ba54-eefd9f8d1fba)
![image](https://github.com/user-attachments/assets/264e2472-8218-4c34-95b8-6a53cf167d44)

| Extension Trigger | Description |
| --- | --- |
| `ggxrd_stateUpdate`| Occurs once a frame. Contains all sorts of cool gamestate data. |
| `ggxrd_hitEvent` | Occurs on Hit or Block. Contains relevant data. |
| `ggxrd_objectCreatedEvent` | Triggers on Object Generation. These can be logic objects, projectiles or special effects. |
| `ggxrd_roundStartEvent` | Triggers on Round Start. |
| `ggxrd_roundEndEvent` | Triggers on Round End. |
| `ggxrd_comboEndEvent` | Combo Summary! Corrals all the data from the last combo. |
| `ggxrd_gamestateDeinitializedEvent` | Triggers when you leave a match or the application closes mid-match. |

### Example of Detecting Level 3 Mist Finer.
This is in the Commands screen of a button set up with the `ggxrd_hitEvent` Extension Trigger. The ggxrd_hitEvent trigger sends along it's own data object that you access with `Trigger Pull Data`.

![image](https://github.com/user-attachments/assets/6b9648ac-ce3d-48cf-8034-be4c6ced3f77)


## More Information

Check out the documentation for [Pangaea's Mod](https://github.com/super-continent/ggxrd-mod) for more information.
