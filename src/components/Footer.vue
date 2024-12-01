<template>
  <footer>
    <p>Bree's PORTFOLIO</p>
  </footer>
</template>

<style lang="scss">
  footer {

    >p{
      color: #E5E3D4;
      font-size: 20px;
      display: flex;
      flex-direction: row;
      justify-content: space-between;
      align-items: center;

      &:after{
        display: block;
        content: " ";
        height: 1px;
        flex: 1 1;
        background-color: #E5E3D4;
        margin-left: 10px;
      }
    }
  }
</style>