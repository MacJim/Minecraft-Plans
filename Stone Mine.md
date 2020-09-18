# Stone Mine

## Features

- Able to generate cobblestone, stone, and smooth stone.
    - Automatically store them separately.
- Able to be used as a super furnace system.
- The whole system resides underground.
- Feed items to smelt by chest minecarts.

## Design

### Cobblestone Generators

Use ilmango's design: <https://www.youtube.com/watch?v=vsWm6F9Ggc4>

One module produces 120,000 cobblestones per hour. That is 1,875 stacks per hour.

Currently I only want to build one such module.

### Furnace Arrays

Use TangoTek's design: <https://youtu.be/Mi4seS507wU?list=WL>

2 such modules. Must keep up with the speed of the cobblestone generators.

#### Amount of Furnaces

It takes 10 seconds to smelt a single item.

Each hour (3,600 seconds), a cobblestone generator module produces 120,000 items.

- 1,200,000 seconds to smelt the items.
- Furnace count = 1,200,000 / 3,600 = 333.33
- Blast furnace count = 333.33 / 2 = 166.67

If we want to generate smooth stone, we'll need to double that amount. That is, 666.67 furnaces.

#### Amount of Fuel

For each furnace array:

- Bamboo: Item count * 4 = 480,000 bamboo per hour = 133.33 per second = 27306 bamboo plants = 106 1D chunks.
    - Bamboo grows approximately every 4096 game ticks (204.8 seconds)
- Carpet: Item count * 3 = 360,000 carpet per hour = 100 per second.
