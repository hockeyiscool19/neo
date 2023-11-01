
   <template>
    <div class="main-container"> 
        
        <div class="left-box">
            <div class="box">
                
                <div class="title">
                    <h3>Hi, I am</h3>
                    <h1>Jordan Eisenman</h1>
                    <h3>Software & Data Engineer</h3>
                </div>
            </div>
        </div>

        <div class="right-box">

            <div class="right-top-box"> 
                <img :src="photo" alt="Description">

            </div>

            <div class="right-bottom-box">
                <div class="slider">
                <div class="slide-track">
                    <div class="slide" v-for="(image, index) in images" :key="index">
                        <img :src="image" alt="" />
                    </div>
                </div>
                </div>
            </div>
            <div>
        </div>

        </div>
    </div>
</template>



<style lang="scss">

.main-container {
    display: flex;      // Enables flexbox layout
}

.left-box {
  width: 40vw;
  height: 100vh;
  background-color: #263238;
  display: flex;           /* Using Flexbox for centering */
  justify-content: flex-start; /* Starts content from the left */
  align-items: center;     /* Vertically centers the content */
  position: relative;      /* To position the title relative to the box */
}

.title {
  text-align: left;
  margin: auto;
  width: 60%;
  border: 3px solid #ECEFF1;
    padding: 10px;
  position: absolute;
  top: 30%;
  left: 10%;
  color: #ECEFF1;  /* This sets the text color to blue */

}

.right-box {
    width: 60vw;
    height: 100vh;
    background-color: #ECEFF1;
    display: flex;           /* Using Flexbox for centering */
    justify-content: center; /* Centers content horizontally */
    align-items: center;     /* Vertically centers the content */
    flex-direction: column; // Add this line to stack child divs vertically.

}

.right-top-box {
    width: 60vw;
    background-color: #ECEFF1;
    display: flex;           /* Using Flexbox for centering */
    justify-content: center; /* Centers content horizontally */
    align-items: center;     /* Vertically centers the content */
    height: 60vh;  // Changed from 60vh to 40vh to take 40% of the parent container's height.

}

.right-bottom-box {
    width: 60vw;
    height: 40vh;
    background-color: #ECEFF1;
    display: flex;           /* Using Flexbox for centering */
    justify-content: center; /* Centers content horizontally */
    align-items: center;     /* Vertically centers the content */
    height: 40vh;  // Changed from 40vh to 60vh to take 60% of the parent container's height.

}

body {
	align-items: center;
	background: #E3E3E3;
	display: flex;
	height: 100vh;
	justify-content: center;
}

@mixin white-gradient {
	background: linear-gradient(to right,  rgba(255,255,255,1) 0%,rgba(255,255,255,0) 100%);
}

$animationSpeed: 40s;

// Animation
@keyframes scroll {
	0% { transform: translateX(0); }
	100% { transform: translateX(calc(-250px * 7))}
}


// Styling
.slider {
    width: 80%;
    height: 10vh; // Match the height of the images
    background: white;
    box-shadow: 0 10px 20px -5px rgba(0, 0, 0, .125);
    margin: auto;
    overflow: hidden;
    position: relative;
    
    &::before,
    &::after {
        height: 10vh; // Match the height of the images
    }
}

.slide-track {
    animation: scroll $animationSpeed linear infinite;
    display: flex;
    width: calc(250px * 14);
    height: 10vh; // Match the height of the images
}

.slide {
    height: 10vh; // Match the height of the images
    width: 10vh; // Match the width of the images
    margin-right: 5vh;  
}

.slide img {
    height: 10vh;
    width: 10vh;
    display: block;
}

</style>

<script lang="ts">

import actions from '../assets/actions.png'
import airflow from '../assets/airflow.png'
import aws from '../assets/aws.png'
import bash from '../assets/bash.png'
import databricks from '../assets/databricks.png'
import docker from '../assets/docker.png'
import firebase from '../assets/firebase.png'
import flask from '../assets/flask.png'
import git from '../assets/git.png'
import gcp from '../assets/gcp.png'
import js from '../assets/js.png'
import k8 from '../assets/k8.png'
import langchain from '../assets/langchain.png'
import mysql from '../assets/mysql.png'
import pg from '../assets/pg.png'
import python from '../assets/python.png'
import rds from '../assets/rds.png'
import s3 from '../assets/s3.png'
import tf from '../assets/tf.png'
import photo from '../assets/personalPhoto.png'

export default {
    name: 'Top',
    data() {
        return {
            images: [
                actions,
                airflow,
                aws,
                bash,
                databricks,
                docker,
                firebase,
                flask,
                git,
                gcp,
                js,
                k8,
                langchain,
                mysql,
                pg,
                python,
                rds,
                s3,
                tf
            ],
            photo: photo
        }
    }
}
</script>