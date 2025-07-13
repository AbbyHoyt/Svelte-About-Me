<script>
    import ImageCard from "./lib/ImageCard.svelte";

    let cardData = [
      {
        image:
          "../src/assets/rainbow.png",
        title: "Color Fanatic 🌈",
        description:
          "I am obsessed with all things colorful! I’m a firm believer that the world needs more color and love to surround myself with happy hues.",
      },
      {
        image: "../src/assets/rover.png",
        title: "TrickFire Robotics 🤖",
        description: 
          "I am a software and marketing member for TrickFire Robotics, the University of Washington Bothell’s University Rover Challenge team!",
      },
      {
        image: "../src/assets/robot.png",
        title: "VEX Robotics 🍋",
        description: 
          "In high school I competed on VRC team 99621A Lemon Pi! My roles on the team consisted of designing, building, programming, and keeping an award-winning 2,200+ page engineering notebook."
      },
      {
        image: "../src/assets/hackathon.png",
        title: "Coding 👩‍💻",
        description: 
          "I love to code! I’ve completed many summer programs and taken CS classes in high school and college. I’m always up to try something new!"
      },
      {
        image: "../src/assets/confetti.png",
        title: "Twin 💕",
        description: 
          "On my dad’s side of the family alone there are three sets of identical twin girls! My twin sister is by far my best friend and partner in crime."
        },
      {
        image: "../src/assets/northernLights.png",
        title: "Washington 🌲",
        description:
          "Although I’ve lived in Washington state my entire life I love exploring new places with my friends. (Yes, it rains a lot here!)"
      },
    ];

  let name = "Abby";
  let favoriteNumber = 192;
  let bio = "Welcome to my (small but colorful) corner of the internet! I live in Washington state and am a student at the University of Washington Bothell. I love coding, robotics, playing flute and piccolo, baking, and spending time with my friends and family.";
  let favorites = ["Coding", "Robotics", "Sprinkles", "The Color Green", "Hippos", "Baking", "Playing Flute and Piccolo", "My Cats", "Strawberry Cake", "Stickers", "The Oort Cloud"];
</script>

<style>
  h1 {
    color: #FF6363;
    font-family: "Quicksand", sans-serif;
  }
  h2 {
    color: #FF6363;
    font-family: "Quicksand", sans-serif;
    font-size: 20pt;
  }
  p {
    color: #000000;
    font-family: "Quicksand", sans-serif;
    font-weight: 500;
  }
  .container {
    max-width: 800px;
    margin: 0 auto;
    padding: 20px;
    text-align: center;
  }
  .favorites {
    display: flex;
    justify-content: center;
    gap: 15px;
    flex-wrap: wrap;
  }
  .favorite {
    background-color: #DBFFCB;
    color: #000000;
    font-family: "Quicksand", sans-serif;
    font-weight: 500;
    padding: 10px 15px;
    border-radius: 5px 15px 5px 15px;
    border: 3px solid #BEE4D0;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  }
  #homeImage {
    border-radius: 50%;
    width: 35%;
    height: auto;
    border: 8px solid #BEE4D0;
    margin-right: auto;
    margin-left: auto;
    display: block;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  }
  .card-container {
    display: inline-flex;
    flex-wrap: wrap;
    justify-content: center;
    align-items: center;
    width: 100%;
  }
  .container {
    border-radius: 20px;
    padding: 35px;
    border: 2px dashed #FF6363;
  }
  * {
    background-color: #FFFFFF;
  }
</style>

<div class="container">
  <img id="homeImage" alt="A headshot of a girl in a green shirt in front of a blue wall." src="../src/assets/abby.jpeg" draggable="false">
  <h1>Hi, I'm {name}! 👋</h1>
  <!--<p>My favorite number is <strong>{favoriteNumber}</strong>.</p>-->
  <p>{bio}</p>

  <br>

  <h2>✨ Things I Love ✨</h2>
  <br>
  <div class="favorites">
    {#each favorites as favorite}
      <div class="favorite">{favorite}</div>
    {/each}
  </div>

  <br>
  <br>

  <h2>✨ About Me ✨</h2>
  <div class="card-container">
    {#each cardData as { image, title, description }}
      <ImageCard {image} {title} {description} />
    {/each}
  </div>
</div>