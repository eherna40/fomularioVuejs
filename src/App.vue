<template lang="pug">
  #app
    .container
      .columns.is-mobile.is-centered
        .column.is-one-third-tablet.is-three-quarters-mobile
          section.hero
            .hero-body
              h1.title SIGN UP
          .form
            .field(v-for='value in dataLabel')
              label.label {{ value.value}}
              .control
                input.input(type="text" placeholder="")
            .field
              label.label CARGO
              .control
                .select
                  select
                    option(v-for="job in jobs" v-bind:value="job.value") {{ job.name}}
            .control
              button.button SIGNUP
            
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      dataLabel:[{
          value: 'NOMBRE',
      },
      {
          value: 'APELLIDO',
      }],
      jobs: [
          {name: 'FullStack JS', value: 'fullstackJs'},
          {name: 'FrontEnd Developer', value: 'frontend'},
          {name: 'Backend Developer', value: 'backend'},
      ],
        selectedJob: 'fullstackJs'
    }
  }
}
</script>

<style lang="scss">
@import './scss/main.scss';
html{
  height: 100vh;
  background: #41295a;
  /* fallback for old browsers */
  background: -webkit-linear-gradient(to right, #2F0743, #41295a);
  /* Chrome 10-25, Safari 5.1-6 */
  background: linear-gradient(to right, #2F0743, #41295a);
  /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */

}

</style>
