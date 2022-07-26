<template lang='pug'>
footer.container.footer-container
    p.footer__content © &nbsp;
    a(href="mailto:info@pakhmutov.ru").footer__email Олег Пахмутов,&nbsp;
    p.footer__content  2009-2022.

</template>


<script>
export default {
  name: 'FooterComponent',
}
</script>

<style lang="scss">

@import "../assets/scss/general.scss";

.footer-container {
    display: flex;
    justify-content: center;
    align-items: center;
    padding-bottom: 30px;
}

.footer__content, .footer__email {
    color: $grayTextColor;
    font-size: 11px;
    font-family: Arial, Helvetica, sans-serif;

    &:hover {
        color:black;
    }
}


</style>