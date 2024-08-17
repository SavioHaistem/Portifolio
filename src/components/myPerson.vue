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
  height: 720px;
  margin-left: 10rem;
}
@media screen and (max-width: 1450px) {
  img.avatar {
    display: none;
    margin: 1rem;
  }
}
@media screen and (max-width: 1046px) {
  img.avatar {
    margin: 0px;
    bottom: -45%;
  }
}

@media screen and (max-width: 920px) {
  img.avatar {
    bottom: -50%;
  }
}
</style>
