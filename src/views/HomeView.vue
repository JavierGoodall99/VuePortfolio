<template>
  <section>
      <div class="top-container container-fluid">
        <img class="astronaut img-fluid" src="https://i.postimg.cc/qBmNgHdx/astronaut.png" alt="astronaut">
        <h1 class="text-black">Hey, I'm Javier Goodall</h1>
        <p class="subheading text-black">Aspiring Full Stack Web Developer</p>
        <img class="spaceship img-fluid" src="https://i.postimg.cc/0yHgJZy3/startup.png" alt="spaceship">
        <img class="moon img-fluid" src="https://i.postimg.cc/PJYBwkRr/halfmoon.png" alt="moon">
        <a href="#" class="link-arrow">
          <img src="https://i.postimg.cc/mkLJ7tnZ/up-arrow.png" loading="lazy" alt="scroll button" class="arrow">
        </a>
      </div>
    </section>
</template>

<script>
export default {
  
}
</script>

<style scoped>
h1 {
    font-size: 50px;
    font-family:'Cinzel', serif;
    animation: fadeIn 5s; 
}
.subheading {
    animation: fadeIn 10s;
}
@keyframes fadeIn {
    0% { opacity: 0; }
    100% { opacity: 3; }
  }
.link-arrow {
    position: fixed;
    bottom: 0.5em;
    right: 0.3em;
}
.arrow {
    width: 40px;
    background-color: white;
}
/* Containers */
.top-container {
    background-color: rgb(82, 97, 107);
    position: relative;
    padding-top: 230px;
}
.telescope {
    width: 100px;
    height: 150px;
    margin: 20px;
}
.skills2 {
    width: 250px;
    height: 300px;
    border-radius: 10%; 
}
/* IMAGES */
.astronaut {
    position: absolute;
    width: 90px;
    height: 80px;
    right: 300px;
    top: 50px;
    
    /* Hover */
    -webkit-animation: mover 2s infinite  alternate;
    animation: mover 2s infinite  alternate;
  }
  @-webkit-keyframes mover {
    0% { transform: translateY(0);
     }
     100% { transform: translateY(-20px); 
    }
  }
  @keyframes mover {
     0% { transform: translateY(0); 
    }
    100% { transform: translateY(-20px); 
    }
  }
.spaceship {
    position: absolute;
    width: 90px;
    height: 80px;
    left: 300px;
    bottom: 300px;

    /* Hover */
    -webkit-animation: mover 2s infinite  alternate;
    animation: mover 2s infinite  alternate;
  }
    @-webkit-keyframes mover {
    0% { transform: translateY(0);
     }
     100% { transform: translateY(-20px); 
    }
  }
  @keyframes mover {
     0% { transform: translateY(0); 
    }
    100% { transform: translateY(-20px); 
    }
  }
.profile1 {
    box-shadow: 0 0 20px 7px black;
}
  
</style>
