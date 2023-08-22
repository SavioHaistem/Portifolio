<template>
   <img class="avatar" src="../assets/images/ReadyPlayerMe-Avatar.png" alt="Avatar">
</template>

<style>
   img.avatar {
      position: absolute;
      width: 300px;
      bottom: -40%;
      left: 0;
      z-index: -1;
      height: 630px;
   }
   @media screen and (max-width: 664px) {
      img.avatar {
         bottom: -50%;
      }
   }
   @media screen and (max-width: 1196px) {
      img.avatar {
         height: 530px;
         width: 250px;
      }
   }
</style>