<template>
   <body>
        <header>
            <div class="header-bottom-furniture wrapper-padding-2 border-top-3">
                <div class="container-fluid">
                    <div class="furniture-bottom-wrapper">
                        <div class="furniture-login">
                            <ul>
                                <li><a href="login.html">Login </a></li>
                                <li><a href="register.html">Register</a></li>
                            </ul>
                        </div>
                    </div>
                </div>
            </div>
        </header>
        <!-- header end -->
		<div class="breadcrumb-area pt-205 pb-210" style="background-image: url(assets/img/bg/header.png)">
            <div class="container">
                <div class="breadcrumb-content text-center">
                    <h2>login</h2>
                    <ul>
                        <li><a href="#">home</a></li>
                        <li> login </li>
                    </ul>
                </div>
            </div>
        </div>
        <!-- login-area start -->
        <div class="register-area ptb-100">
            <div class="container-fluid">
                <div class="row">
                    <div class="col-md-12 col-12 col-lg-6 col-xl-6 ml-auto mr-auto">
                        <div class="login">
                            <div class="login-form-container">
                                <div class="login-form">
                                    <form action="#" method="post">
                                        <input type="text" name="user-name" placeholder="Name">
                                        <input type="text" name="user-email" placeholder="Email">
                                        <input type="password" name="user-password" placeholder="Password">
                                        <div class="button-box">
                                            <button type="submit" class="default-btn floatright">Login</button>
                                        </div>
                                    </form>
                                </div>
                            </div>
                            <a href="register.html">Don't have account? Register here</a>

                        </div>
                    </div>
                </div>
            </div>
        </div>
</template>
<script>
    export default {
    data() {
      return {
        name: '',
        email: '',
        password: ''
      }
    },
    methods: {
        Login: function(){
            let name = this.name
            let email = this.email 
            let password = this.password
            this.$store.dispatch('login', { name, email, password })
            .then(() => this.$router.push('/'))
            .catch(err => console.log(err))
        }
    }
}
<script/>