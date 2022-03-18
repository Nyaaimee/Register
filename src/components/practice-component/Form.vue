<template>
 <div class="container" v-bind:style="{background: activeColor}">
  <h1>{{formTitle}}</h1>
    <form>
      <div>
      <label>First Name *</label>
      <input class="input" type="text" placeholder="First Name">
      </div>
       <div>
      <label>Last Name *</label>
      <input class="input" type="Last Name" placeholder="Last Name">
      </div>
      <div>
        <label>Gender *</label>
        <div class="input2">
        <input  type="radio" name="male">Male
          <input type="radio" name="female">female
         </div>
      </div>
      <div>
        <label>Date Of Birth *</label>
       <input class="input" type="date" id="name" name="name">
      </div>
      <div>
        <label>Age *</label>
        <input class="input" type="number">
      </div>
      <div>
        <label>Address *</label>
        <input class="input" type="text">
      </div>
       <div>
        <label>Contact *</label>
        <input class="input" type="text">
      </div>
      <div>
       <label for="Courses">Courses *</label>
       <select class="input" >
        <option value="Web Development">Web Development</option>
        <option value="Graphic Designer<">Graphic Designer</option>
        <option value="Digital Marketing">Digital Marketing</option>
        <option value="Artificial Intelligence">Artificial Intelligence</option>
       </select>
     </div>

    <button type="submit" @click="handleSubmit">Submit</button>
    </form>
</div> 
</template>


<style>
body{
  background: linear-gradient(to right, teal, orange);

}
.container {
  margin: auto;
  width: 680px;
}
.input{
  display: flex;
  justify-content: space-between;
  width: 20rem;
  height: 2rem;
  /* margin: auto; */
}
.input2{
  display: flex;
}
button {
  width: 6rem;
  height: 2rem;
  margin: 2rem;
  border-radius: 10px;
  position: absolute;
  /* float: right; */
  background: linear-gradient(to left, orange, #0ff);
  transition: ease-in-out 1.5s;
}
button:hover {
  cursor: pointer;
  color: red;
  box-shadow: inset 120px 0 20 0 #000;
}
</style>

<script>
export default {
  name: "form-app",
  data() {
    return {
      firstName: "",
      formTitle: "Student Registration Form",
      activeColor: "teal",
    };
  },
  methods: {
    handleSubmit(x) {
      x.preventDefault();
      this.formTitle = "Form is now submitted no changes can be made";
      this.activeColor = "orange";
    },
  },
};
</script>