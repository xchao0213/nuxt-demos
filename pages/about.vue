<template>
  <div>
    <p>Hi from {{ name }}</p>
    <nuxt-link to="/">Home page</nuxt-link>
    <a-form id='components-form-demo-normal-login' onSubmit={this.handleSubmit} class='login-form'>
        <a-form-item>
         
            <a-input placeholder='Username' />
          
        </a-form-item>
        <a-form-item>
         
            <a-input type='password' placeholder='Password' />
          
        </a-form-item>
        <a-form-item>
         
            <a-checkbox>Remember me</a-checkbox>
          
          <a class='login-form-forgot' href=''>Forgot password</a>
          <a-button type='primary' htmlType='submit' class='login-form-button'>
            Log in
          </a-button>
          Or <a href=''>register now!</a>
        </a-form-item>
      </a-form>
  </div>
</template>

<script>
export default {
  asyncData() {
    return {
      name: process.static ? 'static' : (process.server ? 'server' : 'client')
    }
  },
  head: {
    title: 'About page'
  }
}
</script>