# Sand Simulation
Welcome to your first graphics + simulation task!
In this task, you will be building a sand falling simulator using C++ and the SFML graphics library. You will be simulating sand particles that fall under gravity and interact with each other.
![screenshot](image.png)

## Getting Started
1. To begin create a repository in you Github account and clone it.
2. Install the following packages
- g++ (For compiling and linking)
- SFML (For rendering)

For Ubuntu / Debian / Linux Mint
```
sudo apt-get install build-essential
sudo apt install libsfml-dev
```
For any other distros, refer to [SFML Download guide](https://www.sfml-dev.org/download/sfml/3.0.0/)

3. Create a file named main.cpp and paste the example code
``` C++
#include <SFML/Graphics.hpp>

int main()
{
    sf::RenderWindow window(sf::VideoMode({200, 200}), "SFML works!");
    sf::CircleShape shape(100.f);
    shape.setFillColor(sf::Color::Green);

    while (window.isOpen())
    {
        while (const std::optional event = window.pollEvent())
        {
            if (event->is<sf::Event::Closed>())
                window.close();
        }

        window.clear();
        window.draw(shape);
        window.display();
    }
}
```
4. Compile the code and link to sfml library using g++
```
g++ -c main.cpp
```
5. To link the SFML library
```
g++ main.cpp -o sfml-app -lsfml-graphics -lsfml-window -lsfml-system
```
6. Now simply run `./sfml-app` from terminal.

<b>Happy Coding!</b>