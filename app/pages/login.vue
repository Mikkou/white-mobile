<template>
  <Page class="page">
    <ActionBar title="Войти">
      <NavigationButton @tap="goBack" android.systemIcon="ic_menu_back" text="Назад"/>
    </ActionBar>
    <FlexboxLayout alignItems="center" class="page__container" flexDirection="column">
      <Label text="Email" />
      <TextField class="page__field" width="80%" keyboardType="email" text=""/>
      <Label text="Пароль" />
      <TextField class="page__field" width="80%" text=""/>
      <Button @tap="forgot" class="page__button-forgot" width="40%" text="Забыли пароль?"/>
      <Button @tap="login" class="page__button" width="40%" text="Войти"/>
    </FlexboxLayout>
  </Page>
</template>

<script>
  import Main from '~/pages/main'
  import Forgot from '~/pages/forgot'

  export default {
    name: 'login',
    methods: {
      goBack () {
        this.$navigateTo(Main)
      },
      forgot () {
        this.$navigateTo(Forgot)
      },
      login () {
        alert('Вы авторизовались')
          .then(() => {
            console.log('Alert dialog closed.')
          })
      }
    }
  }
</script>

<style scoped>
  .page__container {
    background-color: #eaeaea;
    color: #A0A0A0;
  }

  .page__field {
    padding: 10 30;
    margin: 10 0;
    border: #A0A0A0;
    background-color: white;
  }

  .page__button {
    background: red;
    border-radius: 5;
    margin: 10 30;
    padding: 20 0;
    color: white;
    font-weight: 600;
  }
</style>
