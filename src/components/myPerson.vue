<template>
  <img class="avatar" src="../../public/images/ReadyPlayerMe-Avatar.png" alt="Avatar" />
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
@media screen and (max-width: 1046px) {
  img.avatar {
    visibility: hidden;
    display: none;
  }
}
</style>
