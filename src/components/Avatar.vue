<style>
div.button {
  position: fixed;
  bottom: 0;
  right: 0;
  width: 5%;
}
</style>

<template>
  <div class = "button">
    <va-button 
    color="#00000000"
    round 
    size="small" 
    @click="showModal = !showModal">
    <img class="user" src="https://icons-for-free.com/iconfiles/png/512/account+circle+24px-131985189042594487.png" height="50">
  </va-button>
  <va-modal
    v-model="showModal"
    :message="message"
    title="User menu"
  />
  </div>
</template>

<script>
export default {
  data() {
    return {
      showModal: false,
      message: 'Here you would find user settings and such',
    };
  },
};
</script>
