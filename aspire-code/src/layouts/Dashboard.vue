<template>
  <div class="row reverse"> 
    <!--img src="../assets/aspire-logo.svg" class="items-end logo"
     alt="AspireLogo"-->

     <q-img src="../assets/aspire-logo.svg" class="items-end logo" > </q-img>
  </div>
  <div class="row acc-card">
    <div class="col-6 fontStyle-14">
      <div class="row padding-10">
        Account balance
      </div>
      <div class="row ">
        <div class="col-3 padding-10">
          <q-badge class="badge"
          color="positive" text-color="white">
          S$
          </q-badge>
        </div>
         <div class="col-4 fontStyle-24">
            3,000
         </div>
      </div>
    </div>

    <div class="col-6 fontStyle-13">
        <div class="row ">
          <div class="col-8 add-card">
            <q-img src="../assets/add-card.svg" class="image"> </q-img>
          </div>
          <div class="col-4 add-card">
            <div> New card </div>
            </div>
        </div>
    </div>

     <q-tabs
        v-model="tab"
        no-caps
        active-color="#ffffff"
                class="text-teal-6"
      >
        <q-tab name="mails" label="Mails" />
        <q-tab name="alarms" label="Alarms" />
        <q-tab name="movies" label="Movies" />
      </q-tabs>


  </div>
</template>

<script>
import { defineComponent, ref } from 'vue'

export default defineComponent({
  setup () {
    return {
      tab: ref('mails')
    }
  },
  name: 'Dashboard',
  data() {
    return {
      logoPath : "../../assets/aspire-logo.svg",
      drawerLeft : false,
      drawerRight : false
    }
  },
  components: {}
 
})
</script>

<style lang="scss">

 .mobile{
   background: #0C365A;
   color: $mobileFontColor;

   .logo{
     margin-top: 16px;
     margin-right: 25px;
     float: right;
     height: 25px;
     width: 25px;
   }

   .add-card > .image{
     width: 16px;
     height: 16px;
   }

   .add-card{
     text-align: right;
     position: relative;
     bottom: 0px;
     right: 12px;
     margin-top: 40px;
     color: #23CEFD;
   }
     
   .acc-card{
     margin: 0px 15px;
   }

  .fontStyle-24{
     font-family: Open Sans;
     font-weight: Bold;
     font-size: 24px;
   }

   .fontStyle-14{
     font-family: Open Sans;
     font-weight: Regular;
     font-size: 14px;
   }

    .fontStyle-13{
     font-family: Open Sans;
     font-weight: Regular;
     font-size: 13px;
   }

   .fontStyle-12{
     font-family: Open Sans;
     font-weight: Regular;
     font-size: 12px;
   }

   .fontStyle-13{
     font-family: Open Sans;
     font-weight: Regular;
     font-size: 13px;
   }

   .padding-10 {
     padding: 7px 0px;
   }

   .badge{
     padding: 3px 10px;
   }
 }
</style>
