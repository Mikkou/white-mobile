<template>
  <Page class="page">
    <ActionBar class="action-bar" title="Home"/>
    <ScrollView>
      <StackLayout class="home-panel">
        <!--Add your page content here-->
        <Label class="h2 description-label test" text="11666555Play with NativeScript!" textWrap="true"/>
        <Label
          class="h2 description-label"
          text="Write code in the editor or drag and drop components to build a NativeScript mobile application."
          textWrap="true"
        />
        <Label
          class="h2 description-label"
          text="Scan the QR code with your mobile device and watch the changes sync live while you play with the code."
          textWrap="true"
        />

        <Button @tap="$navigateTo(detailPage)" class="test" text="To Details directly"/>
      </StackLayout>
    </ScrollView>
  </Page>
</template>

<script>
  export default {
    data () {
      return {
        detailPage: {
          template: `
    <Page>
      <ActionBar title="Detail"/>
      <StackLayout>
        <Label text="Details.." />
      </StackLayout>
    </Page>
  `
        }
      }
    },
  }
</script>

<style scoped>

  .test {
    color: red;
  }


  .home-panel {
    vertical-align: center;
    font-size: 20;
    margin: 15;
  }

  .description-label {
    margin-bottom: 15;
  }
</style>
