<template>
  <div class="footer">
    <span class="text">&#169; Fire-Phoenix.de</span>
    <div class="footer--right">
        <NuxtLink class="link" to="/datenschutz">Datenschutz</NuxtLink>
        <NuxtLink class="link" to="/impressum">Impressum</NuxtLink>
    </div>
  </div>
</template>

<style lang="scss">
    .footer {
        background-color: $color-primary;
        padding: 10px 20px;
        width: 100%;
        position: absolute;
        bottom: 0;

        .text {
            color: $color-white;
        }

        .link {
            color: $color-white;

            &:hover{
                color: $color-third;
                text-decoration: none;
            }
        }

        &--right {
            display: flex;
            gap: 40px;
            float: right;
        }
    }
</style>
