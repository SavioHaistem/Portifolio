<template>
   <img class="avatar" src="../assets/images/ReadyPlayerMe-Avatar.png" alt="Avatar">
</template>

<style>
   img.avatar {
      position: absolute;
      width: 300px;
      bottom: -50%;
      left: 0;
      z-index: -1;
      height: 630px;
   }
   @media screen and (max-width: 664px) {
      img.avatar {
         bottom: -60%;
      }
   }
</style>