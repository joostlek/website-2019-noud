<template>
  <div class="heading">
    <div class="heading-content">
      <img src="/logo/indicium-logo-top.svg" alt="Indicium Logo" />

      <h1>Wij zijn de <span class="bold">studie</span>vereniging voor HBO-ICT van Hogeschool Utrecht</h1>

      <div class="buttons">
        <Button size="l" :onClick="signUp">
          Word lid
        </Button>
        <TextLink :callback="navigateToCalendar">
          Bekijk agenda
        </TextLink>
      </div>
    </div>
  </div>
</template>

<script>
import Button from '../components/interactions/button'
import TextLink from '../components/interactions/TextLink'

export default {
  name: 'Heading',
  components: {
    Button,
    TextLink
  },
  methods: {
    navigateToCalendar() {
      // eslint-disable-next-line no-restricted-globals
      setTimeout(() => { location.href = '#events' }, 1)
    },
    signUp() {
      console.log('kek')
    }
  }
}
</script>

<style lang="scss" scoped>
.heading {
  display: flex;
  justify-content: center;
  padding: 128px 0 192px;

  &-content {
    text-align: center;
    display: flex;
    flex-direction: column;
    align-items: center;

    h1 {
      max-width: 832px;
    }

    .buttons {
      display: flex;
      align-items: center;
      justify-self: center;

      .btn {
        margin-right: 32px;
      }
    }
  }

}
</style>
