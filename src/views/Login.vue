<template>
   <div class="back" id="page-login">
        <div class="div-center">
            <div class="content">
                <h3>Login Ecommerce CMS</h3>
                <hr />
                <form @submit.prevent='login'>
                    <div class="form-group">
                        <label for="email" class="label">Email address</label>
                        <input v-model="email" type="email" class="form-control" id="email" placeholder="Email">
                    </div>
                    <div class="form-group">
                        <label for="password" class="label">Password</label>
                        <input v-model="password" type="password" class="form-control" id="password" placeholder="Password">
                    </div>
                    <button type="submit" class="btn btn-primary label" id="btn-login">Login</button>
                    <hr />
                </form>
                <p>Not having account yet? <a href="" id="link-register">Register Now</a></p>
            </div>
        </div>
    </div>
</template>

<script>
// import axios from '../axios/axios'
export default {
  data () {
    return {
      email: '',
      password: ''
    }
  },
  methods: {
    login () {
      const data = {
        email: this.email,
        password: this.password
      }
      this.$store.dispatch('login', data)
    }
  }
}
</script>

<style scoped>
.back {
  background: #e2e2e2;
  width: 100%;
  position: absolute;
  top: 0;
  bottom: 0;
}

.div-center {
  width: 400px;
  height: 400px;
  background-color: #fff;
  position: absolute;
  left: 0;
  right: 0;
  top: 0;
  bottom: 0;
  margin: auto;
  max-width: 100%;
  max-height: 100%;
  overflow: auto;
  padding: 1em 2em;
  border-bottom: 2px solid #ccc;
  display: table;
}

div.content {
  display: table-cell;
  vertical-align: middle;
}

</style>
