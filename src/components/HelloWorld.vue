<template>
  <form @submit.prevent="submit">
    <section class="form-decor">
      <label for="fullname">Fullname</label><input id="fullname" type="text" v-model="fullname">
    </section>

    <section class="form-decor">
      <label for="occupation">Occupation</label><input type="text" id="occupation" v-model="occupation">
    </section>

    <section class="form-decor">
      <h5>Sex</h5>
      <label for="male">Male</label><input type="radio" id="male" value="male" v-model="sex">
      <label for="female">Female</label><input type="radio" id="female" value="female" v-model="sex">
    </section>

    <section class="form-decor">
      <label for="email">Email</label><input type="email" id="email" v-model="email">
    </section>

    <section class="form-decor">
      <label for="age">Age</label><input type="number" id="age" v-model="age">
    </section>

    <button>Submit</button>

  </form>


</template>

<script>
export default {
  data(){
    return {
      fullname: '',
      occupation: '',
      sex: '',
      email: '',  
      age: ''
    }
  },
  methods: {
    submit(){
      const payload = {
        fullname: this.fullname,
        occupation: this.occupation,
        sex: this.sex,
        email: this.email,
        age: this.age
      }

      console.log(payload)

      //do request here
      // try{
      //   // request here
      // }catch{
      //   alert("something wrong")
      // }
    }
  }

}
</script>

<style>

</style>