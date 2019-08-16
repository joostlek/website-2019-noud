<template>
  <div class="heading">
    <div class="heading-content">
      <img src="/logo/indicium-logo-top.svg" alt="Indicium Logo" />

      <h1>Wij zijn de <span class="medium">studie</span>verenigign voor HBO-ICT van Hogeschool Utrecht</h1>

      <div class="buttons">
        <Button size="l">Wordt lid</Button>
        <TextLink>Bekijk agenda</TextLink>
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
  }
}
</script>

<style lang="scss" scoped>
.heading {
  height: 100vh;
  max-height: 904px;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding-top: 128px;
  background-color: #f2f2f2;

  &-content {
    text-align: center;

    h1 {
      max-width: 568px;
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
