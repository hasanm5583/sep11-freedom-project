# Tool Learning Log

## Tool: **Phaser**

## Project: **Karate Player vs Player game**

---

### 10/19/26:
* cloned the phaser gitub into my ide to
and will fork it so I can learn the lessons as I go weekly since they are on github.  The first Lesson I looked at was animation and how to make animations with the spritesheets 
class Gamescene extends phaser.scene based on research done using phaser as a tool require a npm to include images and music into my game with index.html and CSS and javascript I need assitance getting the npm downloaded on my doe conputer I will come to tutoring and ask on slack and during class for assiatance.Based on my curret research on phaser I'm excited to see how it will handle the physics in my karate game/fight timer.
<script src="//cdn.jsdelivr.net/npm/phaser@3.86.0/dist/phaser.js"></script>
<script src="//cdn.jsdelivr.net/npm/phaser@3.86.0/dist/phaser.min.js"></script> found the CDN!


### 11/03/26:
* 
I learned how to animate a simple sprite from and make repeat on a ellipse and use physics with phaser to make objects bounce off each other. Which I'm sure will be very useful with launching  attacks at opponents in my game. 
class Example extends Phaser.Scene
    {
        preload ()
        {
            this.load.setBaseURL('https://cdn.phaserfiles.com/v385');

            this.load.image('sky', 'assets/skies/space3.png');
            this.load.image('logo', 'assets/sprites/phaser3-logo.png');
            this.load.image('red', 'assets/particles/red.png');
        }

        create ()
        {
            this.add.image(400, 300, 'sky');

            const particles = this.add.particles(0, 0, 'red', {
                speed: 100,
                scale: { start: 1, end: 0 },
                blendMode: 'ADD'
            });

            const logo = this.physics.add.image(400, 100, 'logo');

            logo.setVelocity(100, 200);
            logo.setBounce(1, 1);
            logo.setCollideWorldBounds(true);

            particles.startFollow(logo);
        }
    }

    const config = {
        type: Phaser.AUTO,
        width: 800,
        height: 600,
        scene: Example,
        physics: {
            default: 'arcade',
            arcade: {
                gravity: { y: 200 }
            }
        }
    };
Phaser.Actions.IncXY(myObjects, 4, 6, 1.25, 1.5);
Phaser.Actions.PlaceOnEllipse(myObjects, ellipse, Math.PI * 1.5, Math.PI * 0.5);
    const game = new Phaser.Game(config);
    var json = this.anims.toJSON();

    platforms = this.physics.add.staticGroup(); I can add the image to this code oh my karate teacher when I make it and edit the gravity and ellipse animations from the example from the examples shown on phaser as a guiding tool to then being able to preview it as a sprite of my karate teacher moving!
