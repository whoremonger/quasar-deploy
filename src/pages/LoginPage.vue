<template>
  <q-page class="flex flex-center" padding>

    <div class="full-width" style="max-width: 300px;">
      <h5 class="q-my-md text-center">Login</h5>

      <q-card>
        <q-card-section>
          <q-form>
          <q-input class="q-mb-md" filled placeholder="email@example.com" label="email"/>

          <q-input class="q-mb-sm" filled placeholder="Password" label="password" type="password"/>

          <q-checkbox label="remember me" :model-value="true"/>  
          </q-form>
        </q-card-section>
       
        <q-btn label="Login" class="full-width" color="primary"/>
      </q-card>
    </div>
  </q-page>
</template>

<script>
export default {
  // name: 'PageName',
}
</script>
