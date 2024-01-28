<template>
  <!-- <div class="avatar">
  <img width="130" height="130" src="../assets/profile_pics/pf.jpg" alt="">
</div> -->
  <div class="abat">
    <img src="../assets/profile_pics/pf.jpg" alt="" />
  </div>
</template>
<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "AvatarDisplay",
});
</script>
<style>
.abat img {
  object-fit: cover;
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
  position: relative;
  display: inline-block;
  width: 100%;
  max-width: 150px;
  height: 150px;
  background-repeat: no-repeat;
  background-position: center;
  -webkit-background-size: cover;
  background-size: cover;
}

.abat img {
  --g: 4px; /* the gap */
  --b: 2px; /* border thickness*/
  --c: #5eead5fd; /* the color */

  padding: calc(var(--g) + var(--b));
  --_c: #0000 0 25%, var(--c) 0 50%;
  --_g1: repeating-linear-gradient(90deg, var(--_c)) repeat-x;
  --_g2: repeating-linear-gradient(180deg, var(--_c)) repeat-y;
  background: var(--_g1) var(--_p, 25%) 0, var(--_g2) 0 var(--_p, 125%),
    var(--_g1) var(--_p, 125%) 100%, var(--_g2) 100% var(--_p, 25%);
  background-size: 200% var(--b), var(--b) 200%;
  filter: grayscale(0%);
  transition: 0.3s;
}
.abat img:hover {
  --_p: 75%;
  --c: #5eead5fd; /* the color */
  filter: grayscale(0%);
}

.avatar {
  --border-color: #4255d4;
  --background-color: #212752;
  --avatar-size: 150px;
  height: var(--avatar-size);
  width: var(--avatar-size);
  border: 4px solid var(--border-color);
  padding: 6px;
  border-radius: 50%;
  position: relative;
}
.avatar::before,
.avatar::after {
  content: "";
  position: absolute;
  height: 6px;
  width: 6px;
  transform: rotate(45deg);
  left: 0;
  right: 0;
  top: 0;
  bottom: 0;
  margin: auto;
}
.avatar::before {
  box-shadow: 0px 0px 0px transparent, 4.94975rem 4.94975rem #4255d4,
    0rem 7rem #4255d4, -4.94975rem 4.94975rem #4255d4, -7rem 0rem #4255d4,
    -4.94975rem -4.94975rem #4255d4, 0rem -7rem #4255d4,
    4.94975rem -4.94975rem #4255d4, 7rem 0rem #4255d4;
  -webkit-animation: animate-2 1s ease-in-out infinite;
  animation: animate-2 1s ease-in-out infinite;
}
.avatar::after {
  box-shadow: 0px 0px 0px transparent, 5.54328rem 2.2961rem #4255d4,
    4.24264rem 4.24264rem #4255d4, 2.2961rem 5.54328rem #4255d4,
    0rem 6rem #4255d4, -2.2961rem 5.54328rem #4255d4,
    -4.24264rem 4.24264rem #4255d4, -5.54328rem 2.2961rem #4255d4,
    -6rem 0rem #4255d4, -5.54328rem -2.2961rem #4255d4,
    -4.24264rem -4.24264rem #4255d4, -2.2961rem -5.54328rem #4255d4,
    0rem -6rem #4255d4, 2.2961rem -5.54328rem #4255d4,
    4.24264rem -4.24264rem #4255d4, 5.54328rem -2.2961rem #4255d4,
    6rem 0rem #4255d4;
  transform: rotate(12deg);
  -webkit-animation: animate-1 1s ease-in-out infinite;
  animation: animate-1 1s ease-in-out infinite;
}
.avatar img {
  max-width: 100%;
  height: 100%;
  -o-object-fit: cover;
  object-fit: cover;
  border-radius: inherit;
}

@-webkit-keyframes animate-1 {
  0%,
  100% {
    box-shadow: 0px 0px 0px transparent, 5.54328rem 2.2961rem #4255d4,
      4.24264rem 4.24264rem #4255d4, 2.2961rem 5.54328rem #4255d4,
      0rem 6rem #4255d4, -2.2961rem 5.54328rem #4255d4,
      -4.24264rem 4.24264rem #4255d4, -5.54328rem 2.2961rem #4255d4,
      -6rem 0rem #4255d4, -5.54328rem -2.2961rem #4255d4,
      -4.24264rem -4.24264rem #4255d4, -2.2961rem -5.54328rem #4255d4,
      0rem -6rem #4255d4, 2.2961rem -5.54328rem #4255d4,
      4.24264rem -4.24264rem #4255d4, 5.54328rem -2.2961rem #4255d4,
      6rem 0rem #4255d4;
  }
  50% {
    box-shadow: 0px 0px 0px transparent, 5.08134rem 2.10476rem #4255d4,
      3.88909rem 3.88909rem #4255d4, 2.10476rem 5.08134rem #4255d4,
      0rem 5.5rem #4255d4, -2.10476rem 5.08134rem #4255d4,
      -3.88909rem 3.88909rem #4255d4, -5.08134rem 2.10476rem #4255d4,
      -5.5rem 0rem #4255d4, -5.08134rem -2.10476rem #4255d4,
      -3.88909rem -3.88909rem #4255d4, -2.10476rem -5.08134rem #4255d4,
      0rem -5.5rem #4255d4, 2.10476rem -5.08134rem #4255d4,
      3.88909rem -3.88909rem #4255d4, 5.08134rem -2.10476rem #4255d4,
      5.5rem 0rem #4255d4;
  }
}

@keyframes animate-1 {
  0%,
  100% {
    box-shadow: 0px 0px 0px transparent, 5.54328rem 2.2961rem #4255d4,
      4.24264rem 4.24264rem #4255d4, 2.2961rem 5.54328rem #4255d4,
      0rem 6rem #4255d4, -2.2961rem 5.54328rem #4255d4,
      -4.24264rem 4.24264rem #4255d4, -5.54328rem 2.2961rem #4255d4,
      -6rem 0rem #4255d4, -5.54328rem -2.2961rem #4255d4,
      -4.24264rem -4.24264rem #4255d4, -2.2961rem -5.54328rem #4255d4,
      0rem -6rem #4255d4, 2.2961rem -5.54328rem #4255d4,
      4.24264rem -4.24264rem #4255d4, 5.54328rem -2.2961rem #4255d4,
      6rem 0rem #4255d4;
  }
  50% {
    box-shadow: 0px 0px 0px transparent, 5.08134rem 2.10476rem #4255d4,
      3.88909rem 3.88909rem #4255d4, 2.10476rem 5.08134rem #4255d4,
      0rem 5.5rem #4255d4, -2.10476rem 5.08134rem #4255d4,
      -3.88909rem 3.88909rem #4255d4, -5.08134rem 2.10476rem #4255d4,
      -5.5rem 0rem #4255d4, -5.08134rem -2.10476rem #4255d4,
      -3.88909rem -3.88909rem #4255d4, -2.10476rem -5.08134rem #4255d4,
      0rem -5.5rem #4255d4, 2.10476rem -5.08134rem #4255d4,
      3.88909rem -3.88909rem #4255d4, 5.08134rem -2.10476rem #4255d4,
      5.5rem 0rem #4255d4;
  }
}
@-webkit-keyframes animate-2 {
  0%,
  100% {
    box-shadow: 0px 0px 0px transparent, 3.88909rem 3.88909rem #4255d4,
      0rem 5.5rem #4255d4, -3.88909rem 3.88909rem #4255d4, -5.5rem 0rem #4255d4,
      -3.88909rem -3.88909rem #4255d4, 0rem -5.5rem #4255d4,
      3.88909rem -3.88909rem #4255d4, 5.5rem 0rem #4255d4;
  }
  50% {
    box-shadow: 0px 0px 0px transparent, 4.24264rem 4.24264rem #4255d4,
      0rem 6rem #4255d4, -4.24264rem 4.24264rem #4255d4, -6rem 0rem #4255d4,
      -4.24264rem -4.24264rem #4255d4, 0rem -6rem #4255d4,
      4.24264rem -4.24264rem #4255d4, 6rem 0rem #4255d4;
  }
}
@keyframes animate-2 {
  0%,
  100% {
    box-shadow: 0px 0px 0px transparent, 3.88909rem 3.88909rem #4255d4,
      0rem 5.5rem #4255d4, -3.88909rem 3.88909rem #4255d4, -5.5rem 0rem #4255d4,
      -3.88909rem -3.88909rem #4255d4, 0rem -5.5rem #4255d4,
      3.88909rem -3.88909rem #4255d4, 5.5rem 0rem #4255d4;
  }
  50% {
    box-shadow: 0px 0px 0px transparent, 4.24264rem 4.24264rem #4255d4,
      0rem 6rem #4255d4, -4.24264rem 4.24264rem #4255d4, -6rem 0rem #4255d4,
      -4.24264rem -4.24264rem #4255d4, 0rem -6rem #4255d4,
      4.24264rem -4.24264rem #4255d4, 6rem 0rem #4255d4;
  }
}
</style>
