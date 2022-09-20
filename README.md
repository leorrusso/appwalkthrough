# App Walkthrough

Ever wanted to give few simple instructions to guide your user through your app?
![openfile](/images/img_demo.gif)

## How to install?
The file provided on this repo is of the extension .zip
This is demo app that contains the component. You can work with the component standalone, we will cover it later.
For installing it onto your environment please do the following
1. Create a new canvas app
2. App > Import canvas app > Upload
3. Once the package is loaded open the app

## Context
The component consists of a gallery that displays images and instructions about the app.

## Loading your data
Please use the following schema on the internal component property InstructionCollection. Notice that we used a public link with a gif image. You can also upload the image directly to the app, but I recommend using public links for not overloading the app. You can have as many items as you want.

~~~~
Table(
    {
        id: 1,
        title: "Drag & Drop!",
        image: "https://lowcodera.com/wp-content/uploads/2022/08/SwimlaneGeneral01.gif",
        description: "Drag and drop cards to change their status on the board"
    },
    {
        id: 2,
        title: "Context Menu",
        image: "https://lowcodera.com/wp-content/uploads/2022/08/SwimlaneGeneral02.gif",
        description: "Right click on any card to access interactive options"
    },
    {
        id: 3,
        title: "Master column",
        image: "https://lowcodera.com/wp-content/uploads/2022/08/SwimlaneGeneral03.gif",
        description: "Keep not assigned items separeted before moving anywhere into the board"
    }
)
~~~~

## Showing/Hiding the component
Component visible property should be controled using the global variable "gblFlyoutVisible"

## Responsiveness
Controls X and Y position uses relative formula so the component will always be centered. After adding the component to the screen I recomend setting **Width** for **App.Width** and **Height** for **App.Height**. This will make the component fit different screen sizes. However it is important to mention this will only make subtle adjustments and not fully adapt for any screen size.

## Output property: IdSelectedItem
In case you want to trigger some event related to the instruction, use this property.

## Custom property: _padding
Control the padding of the card

## Custom property: color
Control the color of the circle **(shpCircleStep object)** 

