<template>
  <Page class="page">
    <ActionBar class="action-bar" title="Welcome"/>
    <ScrollView>
      <StackLayout class="home-panel">
        <Image
          class="image"
          src="~/cloud.png"
        />

        <Label
          text="welcome in app!"
          class="welcome-text"
        ></Label>
        <Button class="registration-button" @tap="goToRegistryPage" text="Регистрация"/>
        <Button class="login-button" @tap="goToLoginPage" text="Войти"/>
      </StackLayout>
    </ScrollView>
  </Page>
</template>

<script>
  import Registry from './registry'
  import Login from './login'

  export default {
    methods: {
      goToRegistryPage () {
        this.$navigateTo(Registry)
      },
      goToLoginPage () {
        this.$navigateTo(Login)
      }
    }
  }
</script>

<style scoped>
  .image {
    background: red;
  }

  .welcome-text {
    horizontal-align: center;
    font-size: 30;
    margin: 15;
  }

  .registration-button {
    background: red;
    border-radius: 5;
    margin: 10 30;
    padding: 20 0;
    color: white;
    font-weight: 600;
  }

  .login-button {
    color: red;
    font-weight: 600;
  }

</style>
