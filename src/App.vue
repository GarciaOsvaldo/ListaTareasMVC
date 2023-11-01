<template>
  <div id="app" class="container">
    <div class="menu">
      <div class="logo">
        <img class="perfil" src="./assets/osvaldo.png" alt="Logo" />
        <h4 style="color: white;">Osvaldo García</h4>
      </div>
      <ul class="menu-options">
        <li @click="selectSection('home')" :class="{ active: selectedSection === 'home' }">Home</li>
        <li @click="selectSection('about')" :class="{ active: selectedSection === 'about' }">Sobre mí</li>
        <li @click="selectSection('contact')" :class="{ active: selectedSection === 'contact' }">Contacto</li>
        <li @click="selectSection('projects')" :class="{ active: selectedSection === 'projects' }">Mis Proyectos</li>
        <li @click="selectSection('skills')" :class="{ active: selectedSection === 'skills' }">Habilidades</li>
      </ul>
    </div>
    <div class="content">
      <!-- Sección: Home -->
      <!-- Sección: Home -->
      <h2 style="text-align: center;">Bienvenido a mi portafolio</h2>
<section  id="home" class="home-container" v-show="selectedSection === 'home'">
  
  
</section>
<p style="color: blueviolet; text-align: center;">¡Hola! Mi nombre es Osvaldo García y soy un desarrollador apasionado por crear soluciones innovadoras y efectivas. 
        En mi portafolio puedes encontrar algunos de mis proyectos y habilidades. ¡Gracias por visitar mi sitio!</p>



      <!-- Sección: Sobre Mí -->
      <!-- Sección: Sobre Mí -->
<section id="about" class="section" v-show="selectedSection === 'about'">
  <div id="about-container" class="about-container">
    <h2 style="text-align: center;">Sobre Mí</h2>
    <p style="color: blueviolet;">Como estudiante próximo a finalizar mi técnico en desarrollo de software, 
      mi entusiasmo por el mundo de la programación y el desarrollo de software no tiene límites.
      Durante mi formación, he adquirido habilidades en diferentes lenguajes de programación y 
      he trabajado en proyectos que han ampliado mi comprensión de los conceptos fundamentales.
      Mi enfoque se centra en seguir aprendiendo y perfeccionando mis habilidades para convertirme en un desarrollador capaz.</p>
    <div>
      <p>Si quieres ponerte en contacto escríbeme a:</p>
    </div>
  </div>
</section>


      <!-- Sección: Contacto -->
     <!-- Sección: Contacto -->
<section id="contact" class="section" v-show="selectedSection === 'contact'">
  <div class="contact-container">
    <h1 style="text-align: center; margin-bottom: 20px;">Contáctame</h1>
    <div class="social-media">
      <a href="#" target="_blank" style="margin: 5px;"><img class="social-icon" src="./assets/whatsapp.png" alt="WhatsApp"></a>
      <a href="#" target="_blank" style="margin: 5px;"><img class="social-icon" src="./assets/facebook.png" alt="Facebook"></a>
      <a href="#" target="_blank" style="margin: 5px;"><img class="social-icon" src="./assets/instagram.png" alt="Instagram"></a>
    </div>
    <div class="email">
      <p>Correo electrónico:</p>
      <p>correo@example.com</p>
    </div>
    <div class="technologies-used">
      <h3 style="text-align: center;">ESTE SITIO ESTÁ DESARROLLADO CON:</h3>
      <div class="technologies">
        <div class="technology">
          <img src="./assets/html-5.png" alt="HTML" />
          <p>HTML</p>
        </div>
        <div class="technology">
          <img src="./assets/css.png" alt="CSS" />
          <p>CSS</p>
        </div>
        <div class="technology">
          <img src="./assets/js.png" alt="JavaScript" />
          <p>JavaScript</p>
        </div>
        <div class="technology">
          <img src="./assets/vue.png" alt="Vue.js" />
          <p>Vue.js</p>
        </div>
      </div>
    </div>
  </div>
</section>



      <!-- Sección: Mis Proyectos -->
      <section id="projects" class="section" v-show="selectedSection === 'projects'">
        <h2 style="text-align: center; text-size-adjust: 50px;">Mis Proyectos</h2>
        <div class="projects-container">
          <!-- Proyecto 1 -->
          <div class="project-card" @click="flipCard(1)">
            <div class="card-inner" :class="{ flipped: flippedCard === 1 }">
              <div class="card-front">
                <div class="imagen"><img class="thot" src="./assets/java.png" alt="Thot Project"></div>
                <div class="texto">
                  <p>Aplicación móvil para personas con discapacidad visual</p>
                </div>
              </div>
              <div class="card-back">
                <div class="imagen"><img class="thot" src="./assets/thot.jpeg" alt="Thot Project"></div>
                <div class="texto">
                  <p>Una aplicación móvil que ayuda a las personas con discapacidad visual a navegar por su entorno utilizando comandos de voz y alertas de proximidad.</p>
                </div>
              </div>
            </div>
          </div>

          <!-- Proyecto 2 -->
          <div class="project-card" @click="flipCard(2)">
            <div class="card-inner" :class="{ flipped: flippedCard === 2 }">
              <div class="card-front">
                <div class="imagen"><img class="thot" src="./assets/js.png" alt="Thot Project"></div>
                <div class="texto">
                  <p>Aplicación para agregar tareas</p>
                </div>
              </div>
              <div class="card-back">
                <div class="imagen"><img class="thot" src="./assets/tareas.png" alt="Thot Project"></div>
                <div class="texto">
                  <p>Una aplicación web simple que permite a los usuarios agregar y administrar tareas pendientes de manera eficiente.</p>
                </div>
              </div>
            </div>
          </div>

          <!-- Proyecto 3 -->
          <div class="project-card" @click="flipCard(3)">
            <div class="card-inner" :class="{ flipped: flippedCard === 3 }">
              <div class="card-front">
                <div class="imagen"><img class="thot" src="./assets/html-5.png" alt="Thot Project"></div>
                <div class="texto">
                  <p>Página web para clínica</p>
                </div>
              </div>
              <div class="card-back">
                <div class="imagen"><img class="thot" src="./assets/clinica1.png" alt="Thot Project"></div>
                <div class="texto">
                  <p>Un sitio web interactivo y moderno para una clínica médica que permite a los pacientes reservar citas y acceder a información relevante sobre sus servicios.</p>
                </div>
              </div>
            </div>
          </div>

          <!-- Proyecto 4 -->
          <div class="project-card" @click="flipCard(4)">
            <div class="card-inner" :class="{ flipped: flippedCard === 4 }">
              <div class="card-front">
                <div class="imagen"><img class="thot" src="./assets/js.png" alt="Thot Project"></div>
                <div class="texto">
                  <p>PokeDex</p>
                </div>
              </div>
              <div class="card-back">
                <div class="imagen"><img class="thot" src="./assets/pikachu.png" alt="Thot Project"></div>
                <div class="texto">
                  <p>Una aplicación web que actúa como una enciclopedia de Pokémon, proporcionando a los usuarios información detallada sobre diferentes especies de Pokémon.</p>
                </div>
              </div>
            </div>
          </div>

          

        </div>
      </section>

      
      <!-- Sección: Habilidades -->
<section id="skills" class="section" v-show="selectedSection === 'skills'">
  <div class="skills-container">
    <div>
      <h1 style="text-align: center; margin-bottom: 20px;">Habilidades</h1>
      <h2 style="text-align: center;">Lenguajes de Programación</h2>
      <div class="skills">
        <div class="skill">
          <img src="./assets/java.png" alt="Java" />
          <p>Java</p>
        </div>
        <div class="skill">
          <img src="./assets/js.png" alt="JavaScript" />
          <p>JavaScript</p>
        </div>
        <div class="skill">
          <img src="./assets/cichar.png" alt="C#" />
          <p>C#</p>
        </div>
        <div class="skill">
          <img src="./assets/php.png" alt="PHP" />
          <p>PHP</p>
        </div>
      </div>

      <h2 style="text-align: center;">Frameworks</h2>
      <div class="frameworks">
        <div class="framework">
          <img src="./assets/laravel.png" alt="Laravel" />
          <p>Laravel</p>
        </div>
        <div class="framework">
          <img src="./assets/react.png" alt="React" />
          <p>React</p>
        </div>
        <div class="framework">
          <img src="./assets/vue.png" alt="Vue.js" />
          <p>Vue.js</p>
        </div>
      </div>

      <h2 style="text-align: center;">Herramientas</h2>
      <div class="tools">
        <div class="tool">
          <img src="./assets/vsCode.png" alt="Visual Studio Code" />
          <p>Visual Studio Code</p>
        </div>
        <div class="tool">
          <img src="./assets/GitHub12.png" alt="GitHub" />
          <p>GitHub</p>
        </div>
      </div>
    </div>
  </div>
</section>

    </div>
    
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      selectedSection: 'home',
      flippedCard: null
    };
  },
  methods: {
    selectSection(section) {
      this.selectedSection = section;
    },
    flipCard(cardNumber) {
      if (this.flippedCard === cardNumber) {
        this.flippedCard = null;
      } else {
        this.flippedCard = cardNumber;
      }
    },
    changeTextColor() {
      setInterval(() => {
        const aboutContainer = document.getElementById('about-container');
        const paragraphs = aboutContainer.getElementsByTagName('p');
        for (let i = 0; i < paragraphs.length; i++) {
          const r = Math.floor(Math.random() * 256);
          const g = Math.floor(Math.random() * 256);
          const b = Math.floor(Math.random() * 256);
          const color = `rgb(${r}, ${g}, ${b})`;
          paragraphs[i].style.color = color;
        }
      }, 2000);
    }
  },
  mounted() {
    this.changeTextColor();
  }
};
</script>

<style>
  /* Agregué estilos para el contenedor principal */
  .container {
    display: flex;
    flex-direction: row;
    align-items: stretch;
  }

  /* Estilos para la sección de home */
.home-container {
  display: flex;
  justify-content: center;
  align-items: center;
  /* Ajusta el tamaño y margen según tus necesidades */
  height: 400px; /* Altura deseada */
  margin: 0; /* Elimina el margen para que la imagen sea visible */
  background-image: url('./assets/fondo.jpg');
  background-size: cover; /* Ajusta el tamaño de la imagen para cubrir todo el contenedor */
  background-position: center; /* Centra la imagen horizontalmente y verticalmente */
  border: 2px solid #4caf50;
  border-radius: 10px;
  padding: 20px;
  background-color: #f3f3f3;
}

.home-content {
  text-align: center;
}


  /* Estilos para el menú */
  .menu {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 20px;
    background-color: #3949ab;
    height: 100vh;
    color: white;
    width: 200px;
    position: fixed;
  }

  .logo {
    text-align: center;
    margin-bottom: 20px;
  }

  .menu-options {
    list-style-type: none;
    padding: 0;
    width: 100%;
  }

  .menu-options li {
    padding: 10px 0;
    cursor: pointer;
    transition: background-color 0.3s;
  }

  .menu-options li.active {
    background-color: #fbc02d;
  }

  /* Estilos para el contenido */
  .content {
    flex: 1;
    padding: 20px;
    margin-left: 200px;
  }

  /* Alinea el contenido a la derecha del menú */
  #about,
  #contact,
  #projects,
  #skills {
    text-align: right;
  }

 


  /* Estilos para la sección de proyectos */
  .projects-container {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    align-items: center;
  }

  .project-card {
    margin: 20px;
    width: 200px;
    perspective: 1000px;
  }

  .card-inner {
    position: relative;
    width: 100%;
    height: 100%;
    text-align: center;
    transition: transform 0.8s;
    transform-style: preserve-3d;
  }

  .card-inner.flipped {
    transform: rotateY(180deg);
  }

  .card-front,
  .card-back {
    position: absolute;
    width: 100%;
    height: 100%;
    backface-visibility: hidden;
  }

  .card-back {
    transform: rotateY(180deg);
  }



  /* Estilos para la sección de habilidades */
  /* Estilos para la sección de habilidades */
.skills-container {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  margin-top: 20px;
}

.skills,
.frameworks,
.tools {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-top: 20px;
}

.skill,
.framework,
.tool {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 10px;
}

.skill img,
.framework img,
.tool img {
  width: 80px;
  height: 80px;
  border-radius: 50%;
  border: 3px solid #4caf50;
  padding: 5px;
}

.skill p,
.framework p,
.tool p {
  margin-top: 10px;
  font-size: 1.2em;
  color: #4caf50;
}

/* Estilos para la sección de contacto *//* Estilos para la sección de contacto */
.contact-container {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.social-media {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-top: 20px;
}

.social-icon {
  width: 30px;
  height: 30px;
  margin: 5px;
  transition: transform 0.3s;
}

.social-icon:hover {
  transform: scale(1.2);
}

.email {
  margin-top: 20px;
  text-align: center;
}

.technologies-used {
  margin-top: 20px;
  text-align: center;
}

.technologies {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-top: 20px;
}

.technology {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 10px;
}

.technology img {
  width: 80px;
  height: 80px;
  border-radius: 50%;
  border: 3px solid #4caf50;
  padding: 5px;
}

.technology p {
  margin-top: 10px;
  font-size: 1.2em;
  color: #4caf50;
}

/* Estilos para la sección de home */
.home-container {
  display: flex;
  justify-content: center;
  align-items: center;
  margin: 50px;
  border: 2px solid #4caf50;
  border-radius: 10px;
  padding: 20px;
  background-color: #f3f3f3;
}

.home-content {
  text-align: center;
}

/* Estilos para la sección de Sobre Mí */
.about-container {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  text-align: center;
  font-family: 'cursive', cursive;
}

.about-container p {
  transition: color 2s;
}




</style>
