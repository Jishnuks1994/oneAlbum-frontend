<script>
  let isMenuOpen = false;

  function toggleMenu() {
    isMenuOpen = !isMenuOpen;
  }
</script>

<header class="inset-x-0 top-0 z-50">
  <nav class="flex items-center justify-between p-6 lg:px-8" aria-label="Global">
    <div class="flex lg:flex-1">
      <a href="/" class="-m-1.5 p-1.5 flex lg:flex-1">
          <img class="h-8 w-auto me-3" src="https://tailwindui.com/img/logos/mark.svg?color=indigo&shade=600" alt="logo">
          <span class="text-3xl antialiased font-semibold font-sans">One Album</span>
      </a>
    </div>
    <div class="flex lg:hidden">
      <!-- Toggle button for mobile menu -->
      <button type="button" class="-m-2.5 inline-flex items-center justify-center rounded-md p-2.5 text-gray-700" on:click={toggleMenu}>
        <span class="sr-only">Open main menu</span>
        <svg class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" aria-hidden="true">
          <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
        </svg>
      </button>
    </div>
    <div class="hidden lg:flex lg:gap-x-12">
      <a href="#" class="text-sm font-semibold leading-6 text-gray-900">Product</a>
      <a href="/pricing" class="text-sm font-semibold leading-6 text-gray-900">Pricing</a>
      <a href="#" class="text-sm font-semibold leading-6 text-gray-900">Customers</a>
      <a href="#" class="text-sm font-semibold leading-6 text-gray-900">Examples</a>
    </div>
    <div class="hidden lg:flex lg:flex-1 lg:justify-end lg:gap-x-12">
      <a href="/login" class="text-sm rounded-md px-3.5 py-2.5 font-semibold leading-6 text-white bg-blue-500 bg-opacity-90">Log in</a>
      <a href="#" class="text-sm font-semibold px-3.5 py-2.5 leading-6 text-gray-900">Try for Free</a>
    </div>
  </nav>

  <!-- Mobile menu, show/hide based on menu open state. -->
  <div class="{`lg:hidden ${isMenuOpen ? 'block' : 'hidden'}`}" role="dialog" aria-modal="true">
    <!-- Background backdrop, show/hide based on slide-over state. -->
    <div class="fixed inset-0 z-50" on:click={toggleMenu}></div>
    <div class="fixed inset-y-0 right-0 z-50 w-full overflow-y-auto bg-white px-6 py-6 sm:max-w-sm sm:ring-1 sm:ring-gray-900/10">
      <div class="flex items-center justify-between">
        <a href="#" class="-m-1.5 p-1.5">
          <span class="sr-only">One Album</span>
          <img class="h-8 w-auto" src="https://tailwindui.com/img/logos/mark.svg?color=indigo&shade=600" alt="">
        </a>
        <button type="button" class="-m-2.5 rounded-md p-2.5 text-gray-700" on:click={toggleMenu}>
          <span class="sr-only">Close menu</span>
          <svg class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" aria-hidden="true">
            <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
          </svg>
        </button>
      </div>
      <div class="mt-6 flow-root">
        <div class="-my-6 divide-y divide-gray-500/10">
          <div class="space-y-2 py-6">
            <a href="#" class="-mx-3 block rounded-lg px-3 py-2 text-base font-semibold leading-7 text-gray-900 hover:bg-gray-50">Product</a>
            <a href="#" class="-mx-3 block rounded-lg px-3 py-2 text-base font-semibold leading-7 text-gray-900 hover:bg-gray-50">Pricing</a>
            <a href="#" class="-mx-3 block rounded-lg px-3 py-2 text-base font-semibold leading-7 text-gray-900 hover:bg-gray-50">Customers</a>
            <a href="#" class="-mx-3 block rounded-lg px-3 py-2 text-base font-semibold leading-7 text-gray-900 hover:bg-gray-50">Examples</a>
          </div>
          <div class="py-6">
            <a href="/login" class="-mx-3 block rounded-lg px-3 py-2.5 text-base font-semibold leading-7 text-gray-900 hover:bg-gray-50">Log in</a>
            <a href="#" class="-mx-3 block rounded-lg px-3 py-2.5 text-base font-semibold leading-7 text-gray-900 hover:bg-gray-50">Try for Free</a>
          </div>
        </div>
      </div>
    </div>
  </div>
</header>
