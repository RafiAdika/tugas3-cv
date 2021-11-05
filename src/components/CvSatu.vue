<template>
    <div id="c">
        <h1 style="margin-left:300px;">CV-1</h1> 
        <div id="a">
            <div v-for="cv in listCv" :key="cv"> 
            <div id="d"> 
                <h2>{{cv.a1}}<font id="e"><br>{{cv.a2}}</font> 
                </h2> 
                <img src="photo.jpg" width="250" height="150"> 
                <h3>{{cv.a3}}
                    <hr> 
                </h3> 
                <p>{{cv.a4}}<br>{{cv.a5}}</p> 
                <p>{{cv.b1}}<br>{{cv.b2}}</p> 
                <p>{{cv.b3}}<br><u>{{cv.b4}}</u></p> 
                <p>{{cv.b5}}<br>-</p> 
                <h3>{{cv.c1}} 
                    <hr> 
                </h3> 
                <ul>
                <li>{{cv.c2}}<br><li>{{cv.c3}}<br><li>{{cv.c4}}</li>
                </ul> 
                <h3>{{cv.c5}} 
                    <hr> 
                </h3> 
                <ul>
                <li>{{cv.d1}}<br><li>{{cv.d2}}<br><li>{{cv.d3}}<br><li>{{cv.d4}}</li>
                </ul> 
            </div> 
            <div id="b"> 
                <h2>{{cv.d5}}</h2>
        <hr />
        <p>{{cv.d6}}<br>{{cv.d7}}<br>{{cv.d8}}<br>{{cv.d9}}<br>S{{cv.d10}}</p>

     <h2>{{cv.d11}}</h2>
     <hr />
     <div style="display: flex;">
         <div>
            <ul>
                <li>{{cv.d12}}</li>
                <li>{{cv.d13}}</li>
                <li>{{cv.d14}}</li>
           </ul>       
         </div>
         <div>
<ul>
    <li>{{cv.d15}}</li>
    <li>{{cv.d16}}</li>
    <li>{{cv.d17}}</li>

</ul>
         </div>
        </div>
     <h2>{{cv.d18}}</h2>
     <hr />
     <h4>{{cv.d19}}</h4>
     <h4>{{cv.d20}}</h4>
     <ul>
         <li>{{cv.d21}}<br>{{cv.d22}}</li>
         <li>{{cv.d23}}</li>
         <li>{{cv.d24}}<br>{{cv.d25}}</li>
         <li>{{cv.d26}}<br>{{cv.d27}}</li>
    <h2>{{cv.d28}}</h2>
        <hr />
        <p>{{cv.d29}}<br>{{cv.d30}}</p>
    <h2>{{cv.d31}}</h2>
        <hr />
        <p>{{cv.d32}}<br>{{cv.d33}}</p>
     </ul> 
            </div> 
        </div>
        </div> 
    </div>
</template>
<script>
/* eslint-disable */
import axios from "axios";
export default {
  data() {
    return {
      listCv: [],
    };
  },
  mounted() {
    this.load();
  },
  methods: {
    load() {
      axios
        .get("http://localhost:3000/listCv")
        .then((res) => {
          this.listCv = res.data;
        })
        .catch((err) => {
          console.log(err);
        });
    },
  },
  name: "CvSatu",
  computed: {
    listCv() {
      return this.$store.state.listCv;
    },
  },
};
</script>

<style>
#a { 
    display: flex; 
    background-color: rgb(189, 189, 189); 
    padding-left: 20px;
    margin-top: 20px;
    width: 350px; 
} 
#b { 
    background-color: white; 
    padding-left: 10px;
    margin-left: 351px;
    margin-top: -800px;
} 
#c { 
    margin-right: 300px; 
    padding-left: 100px; 
} 
#d { 
    font-family: sans-serif; 
    padding-right: 35px; 
} 
#e { 
    color: rgb(255, 102, 0); 
} 
hr { 
    border: none; 
    height: 1px; 
    /* Set the hr color */ 
    color: black; /* old IE */ 
    background-color: black; /* Modern Browsers */ 
    width: 100%; 
}
</style>