<template>
  <q-layout>
    <q-page-container>
      <q-page class="flex flex-center" style="font-family: Lato;">
<!--        <div id="particles-js"></div>-->
        <q-card :style="$q.platform.is.desktop ? 'width:55%;' : ''" class="row my-card items-center q-pa-none q-ma-none shadow-24">
          <q-card-section v-if="$q.platform.is.desktop" class="col-md-4 col-lg-4 col-sm-12 sol-xs-12 items-center float-left" style="background-color: #d5ccc0"
                          :style="{'height':(win_height-270)+'px'}" horizontal>
            <div class="text-center full-width">
              <div><img src="images/cover.png" style="width: 90%"/></div>
              <!-- <div class="text-weight-bolder text-white text-h6">Quasar Shopping</div> -->
              <div class="text-caption text-white q-px-xs">Produtos frescos, cuidadosamente selecionados.</div>
            </div>
          </q-card-section>
          <q-card-section class="col-md-8 col-lg-8 col-sm-12 sol-xs-12 float-left">
            <q-card-section class="items-center">
              <div>
                <div v-if="!$q.platform.is.desktop" class="text-weight-bolder text-center q-mb-md text-primary text-h6">Quasar Shopping</div>
                <q-form :style="$q.platform.is.desktop ? 'width:55%;margin: auto;' : 'margin: auto;'" class="q-gutter-md">
                  <span class="text-subtitle1 text-weight-bold text-grey-7">Bem-Vindo/a!</span>
                  <q-input
                    dense
                    outlined
                    v-model="username"
                    label="E-mail"
                    lazy-rules
                  />

                  <q-input
                    dense
                    type="password"
                    outlined
                    v-model="password"
                    label="Senha"
                    lazy-rules
                  />
                  <q-checkbox class="text-grey-8" dense v-model="remember_me" label="Lembrar"/>
                  <div>
                    <q-btn class="text-capitalize text-white" size="sm" style="width:75px; background-color:#9e7d65; " dense label="Iniciar Sessão" to="/home" type="button"
                           />
                    <q-btn class="float-right text-capitalize text-brown" size="sm" style="width:75px;border: 1px solid #9e7d65;" dense label="Criar conta"
                           type="button"/>
                  </div>
                </q-form>

              </div>
            </q-card-section>
          </q-card-section>

        </q-card>
      </q-page>
    </q-page-container>
  </q-layout>
</template>

<script>
    export default {
        data() {
            return {
                username: 'mayur',
                password: 'mayur@qu',
                remember_me: false
            }
        },
        mounted() {

        },
        computed: {
            win_width() {
                return this.$q.screen.width - 59;
            },
            win_height() {
                return this.$q.screen.height - 0;
            }
        }
    }
</script>
<style>
  .my-card {
    /*width: 55%;*/
    height: 30%;
  }

  #particles-js {
    position: absolute;
    width: 100%;
    height: 100%;
    /*background: linear-gradient(145deg, #abbaab 15%, #ffffff 70%);*/
    /*background: linear-gradient(145deg,#f7f8f8 11%, #627e79 75%);*/
    background-repeat: no-repeat;
    background-size: cover;
    background-position: 50% 50%;
  }

  .login-form {
    position: absolute;
  }
</style>
