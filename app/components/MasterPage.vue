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
        <Button class="registration-button" @tap="$navigateTo(registryPage)" text="Регистрация"/>
        <Button class="login-button" @tap="$navigateTo(loginPage)" text="Войти"/>
      </StackLayout>
    </ScrollView>
  </Page>
</template>

<script>

  const RegistryPage = {
    template: `
            <Page>
              <ActionBar title="Registration"/>
              <GridLayout columns="auto,100" rows="auto,auto" width="300" height="300" backgroundColor="lightgray" >
                <Label text="register form" col="0" row="0" backgroundColor="red"/>
                <Label text="Label 2" col="1" row="0" backgroundColor="green"/>
                <Label text="Label 3" width="150" col="0" row="1" backgroundColor="blue"/>
              </GridLayout>
            </Page>
          `
  }

  const LoginPage = {
    template: `
            <Page>
              <ActionBar title="Authorisation"/>
              <StackLayout>
                <Label text="auth form"/>
              </StackLayout>
            </Page>
          `
  }

  export default {
    data () {
      return {
        registryPage: RegistryPage,
        loginPage: LoginPage
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
