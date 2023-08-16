<template>
   <img class="avatar" src="../assets/images/ReadyPlayerMe-Avatar.png" alt="Avatar">
</template>

<style>
   img.avatar {
      position: absolute;
      width: 400px;
      bottom: -50%;
      left: 0;
      z-index: -1;
      height: 830px;
   }
   @media screen and (max-width: 664px) {
      img.avatar {
         bottom: -60%;
      }
   }
   @media screen and (max-width: 1196px) {
      img.avatar {
         height: 630px;
         width: 300px;
      }
   }
</style>