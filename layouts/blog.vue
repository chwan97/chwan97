<template>
  <div class="container">
    <CThemeProvider>
      <CColorModeProvider>
        <CBox font-family="body" as="main">
          <CReset />
          <div class='all-title'>CHWAN > 关于我</div>
          <Nuxt />
        </CBox>
      </CColorModeProvider>
    </CThemeProvider>
  </div>
</template>

<style>
.all-title {
  background-color: #2030a0;
  color: #fff;
  width: 100vw;
  padding: 2px 20px;
  margin: -15px;
}
</style>

<script>
import {
  CThemeProvider,
  CColorModeProvider,
  CReset,
  CBox
} from '@chakra-ui/vue'

export default {
  name: 'DefaultLayout',
  components: {
    CThemeProvider,
    CColorModeProvider,
    CReset,
    CBox
  }
}
</script>
