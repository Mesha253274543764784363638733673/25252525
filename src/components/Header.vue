<script setup>
defineProps({
    totalPrice: Number
})

const emit = defineEmits(['toggleDrawer']) // Определяем функцию для передачи события toggleDrawer
</script>

<template>
  <header class="flex justify-between border-b border-slate-200 px-8 py-8">
    <RouterLink to="/">
        <div class="flex items-center gap-4">
           
            <img src="/logo.png" alt="image" class="w-40" />
        
            <div>
                <h2 class="text-xl font-bold uppercase">Portal Lider</h2>
            
                <p class="text-slate-400">Магазин игр</p>
            
            </div>
           
    
        </div>
    </RouterLink>
    <ul class="flex items-center gap-10">
      
      <li
        @click="() => emit('toggleDrawer')"
        class="flex items-center cursor-pointer gap-3 text-gray-500 hover:text-black"
      >
        <img src="/cart.svg" alt="" />
        
        <b>{{ totalPrice }} ₸</b>
      
      </li>
      <li class="flex items-center cursor-pointer gap-3 text-gray-500 hover:text-black">
       
        <img src="/heart.svg" alt="" />
       
        <RouterLink to="/favorites"><span>Лайкнутые</span></RouterLink>
        
      </li>
      <li class="flex items-center cursor-pointer gap-3 text-gray-500 hover:text-black">
      
        <img src="/profile.svg" alt="" />
     
        <span>Профиль</span>
        <!-- Текст элемента -->
      </li>
      <li class="flex items-center cursor-pointer gap-3 text-gray-500 hover:text-black">
      
      <img src="/r.png" alt="" class="w-6"/>
   
      <span>Баланс</span>
      <!-- Текст элемента -->
    </li>
    </ul>
  </header>
</template>
