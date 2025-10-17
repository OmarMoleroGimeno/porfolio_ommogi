<script setup>
import TextType from '@/components/TextAnimations/TextType/TextType.vue';
import RadioButton from '@/components/Buttons/RadioButton.vue';
import CurriculumButton from '@/components/Buttons/CurriculumButton.vue';
import ProfileCard from '@/components/Components/ProfileCard/ProfileCard.vue';
import iconpatternUrl from '@/assets/img/iconpattern.png';
import grainUrl from '@/assets/img/grain.webp';
import stickerUrl from '@/assets/img/sticker-omar.png';
import { ArrowBigDownDash } from 'lucide-vue-next';

const handleContactClick = () => {
    console.log('Contact button clicked!');
};
</script>
<template>
    <div class="flex h-screen relative">
        <div class="flex flex-col justify-center align-middle">
            <div>
            <h1 class="text-6xl font-bold mb-4 text-black dark:text-white">Hola, soy Omar Molero Gimeno</h1>
            <div class="flex">
                <h2 class="text-4xl">un diseñador</h2>
                <TextType 
                :text="[' Web', ' UX', ' UI']"
                :typingSpeed="75"
                :pauseDuration="3000"
                :showCursor="true"
                cursorCharacter="_"
                class-name="text-4xl"
                :textColors="['#ffb029', '#ffb029', '#ffb029']"
                />
            </div>
            <p class="text-lg mt-8 text-black dark:text-white">
                Desarrollador Frontend especializado en transformar diseños y conceptos en experiencias web atractivas, 
                funcionales y de alto rendimiento. Mi enfoque se centra en construir interfaces de usuario intuitivas 
                y optimizar la experiencia de usuario mediante código limpio, mantenible y escalable.Hola, soy 
            </p>
            </div>
            
            <div class="flex flex-row gap-4 mt-8">
            <RadioButton text="github" url="https://github.com/omarmolerogimeno">
                <svg viewBox="0 0 192 192" xmlns="http://www.w3.org/2000/svg" height="25" fill="none">
                <path class="stroke-black dark:stroke-white"stroke-linecap="round" stroke-linejoin="round" stroke-width="12" 
                    d="M120.755 170c.03-4.669.059-20.874.059-27.29 0-9.272-3.167-15.339-6.719-18.41 
                    22.051-2.464 45.201-10.863 45.201-49.067 0-10.855-3.824-19.735-10.175-26.683 
                    1.017-2.516 4.413-12.63-.987-26.32 0 0-8.296-2.672-27.202 10.204-7.912-2.213-16.371-3.308-24.784-3.352
                    -8.414.044-16.872 1.14-24.785 3.352C52.457 19.558 44.162 22.23 44.162 22.23
                    c-5.4 13.69-2.004 23.804-.987 26.32C36.824 55.498 33 64.378 33 75.233
                    c0 38.204 23.149 46.603 45.2 49.067-3.551 3.071-6.719 9.138-6.719 18.41
                    0 6.416.03 22.621.059 27.29M27 130c9.939.703 15.67 9.735 15.67 9.735
                    8.834 15.199 23.178 10.803 28.815 8.265">
                </path>
                </svg>
            </RadioButton>
            <RadioButton text="linkedin" url="https://www.linkedin.com/in/omar-molero-gimeno-33526b2aa/">
                <svg class="fill-black dark:fill-white" height="17" viewBox="0 0 310 310">
                <path d="M72.16,99.73H9.927c-2.762,0-5,2.239-5,5v199.928c0,2.762,2.238,5,5,5H72.16c2.762,0,5-2.238,5-5V104.73 
                    C77.16,101.969,74.922,99.73,72.16,99.73z"></path>
                <path d="M41.066,0.341C18.422,0.341,0,18.743,0,41.362C0,63.991,18.422,82.4,41.066,82.4
                    c22.626,0,41.033-18.41,41.033-41.038C82.1,18.743,63.692,0.341,41.066,0.341z"></path>
                <path d="M230.454,94.761c-24.995,0-43.472,10.745-54.679,22.954V104.73c0-2.761-2.238-5-5-5h-59.599
                    c-2.762,0-5,2.239-5,5v199.928c0,2.762,2.238,5,5,5h62.097c2.762,0,5-2.238,5-5v-98.918
                    c0-33.333,9.054-46.319,32.29-46.319c25.306,0,27.317,20.818,27.317,48.034v97.204c0,2.762,2.238,5,5,5H305
                    c2.762,0,5-2.238,5-5V194.995C310,145.43,300.549,94.761,230.454,94.761z">
                </path>
                </svg>
            </RadioButton>
            <CurriculumButton />
            </div>
        </div>
        <div class="w-[390px] flex flex-col justify-center align-middle"> 
            <ProfileCard
                name="Omar M. G."
                title="Desarrollador Frontend"
                handle="ommogi"
                status="En línea"
                contact-text="Contáctame"
                :avatar-url="stickerUrl"
                :icon-url="iconpatternUrl"
                :grain-url="grainUrl"
                :show-user-info="true"
                :show-behind-gradient="true"
                :enable-tilt="true"
                @contact-click="handleContactClick"
            />
        </div>
        <ArrowBigDownDash class="absolute bottom-5 left-1/2 -translate-x-1/2 w-10 h-10 text-[#ffb029] animate-bounce-y" />
    </div>
    
</template>
<style>
@keyframes bounce-y {
  0%, 100% {
    transform: translateY(-25%);
    animation-timing-function: cubic-bezier(0.8, 0, 1, 1);
  }
  50% {
    transform: translateY(0);
    animation-timing-function: cubic-bezier(0, 0, 0.2, 1);
  }
}

.animate-bounce-y {
  animation: bounce-y 1s infinite;
}
</style>