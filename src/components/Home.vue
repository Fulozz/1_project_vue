<template>
    <main>
        <div class="text-top"> Vídeos novos toda <b>quinta</b> as 20horas</div>

        <a href="https://youtube.com/" target="_blank">
        <img id="subscribe" src="https://raw.githubusercontent.com/william-costa/wdev-mock-site-resources/master/assets/images/subscribe.svg" alt="inscreva-se">
        </a>

         <div class="text-bottom"> youtube.com/fulozz</div>
    </main>

</template>

<script>
export default {
    name: 'HomePage'
}
</script>


<style scoped>

main{
    background-color: var(--color-background-home);
    justify-content: center;
    text-align: center;
}
.text-top{
    color: var(--color-text-light);
    font-size: 22px;
    margin-bottom: 20px;
}
.text-bottom{
    color: var(--color-text-light);
    font-size: 18px;
    margin-top: 20px;
}
#subscribe{
    width: 340px;
}

@media (min-width: 768px) {
    #subscribe{
    width: 370px;   
    } 
}

</style>