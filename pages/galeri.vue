<template>
   <div class="container-fluid">
        <div class="heading pt-4 ">
            <h1 class="text-center text-black pt-4">  Gallery </h1>
        </div>
        <div class="row py-5 px-lg-5 px-sm-0">
            <div class="column">
                <img src="assets/1.png" class="h:scale-1" alt="" srcset="">
                <img src="assets/3.png" alt="" srcset="">
            </div>
            <div class="column">
                <img src="assets/2.png" alt="" srcset="">
                <img src="assets/4.png" alt="" srcset="">

            </div>
            <div class="column">
                <img src="assets/5.jpg" alt="" srcset="">
                <img src="assets/6.jpg" alt="" srcset="">
            </div>
            <div class="column">
                <img src="assets/7.jpg" alt="" srcset="">
                <img src="assets/8.jpg" alt="" srcset="">
            </div>
        </div>
   </div>
</template>
<style scoped>
.row {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(100px, 1fr));
        }
        .column {
            grid-column: span 3;
            width: auto;
            height: 100%;
            overflow: hidden;
            display: flex;
            flex-direction: column;
            gap: 1rem;
        }
</style> 