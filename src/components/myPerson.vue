<template>
  <img class="avatar" src="../../public/images/ReadyPlayerMe-Avatar.png" alt="Avatar" />
</template>

<style>
img.avatar {
  position: absolute;
  width: 350px;
  bottom: -30%;
  left: 0;
  z-index: -1;
  height: 700px;
}
@media screen and (max-width: 1046px) {
  img.avatar {
    bottom: -45%;
  }
}

@media screen and (max-width: 920px) {
  img.avatar {
    bottom: -50%;
  }
}
</style>
