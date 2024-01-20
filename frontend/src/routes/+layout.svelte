<script>
  import "../app.css";

  let screenWidth;
</script>

<svelte:window bind:innerWidth={screenWidth} />

{#if screenWidth < 800}
<div>
  Mobile not supported. Please view on a desktop screen!
</div>
{:else}

<div>
  <!-- Static sidebar for desktop -->
  <div class="hidden lg:fixed lg:inset-y-0 lg:z-50 lg:flex lg:w-72 lg:flex-col">
    <!-- Sidebar component, swap this element with another sidebar if you like -->
    <div class="flex grow flex-col gap-y-5 overflow-y-auto bg-gray-900 px-6 pb-4">
      <div class="flex h-16 shrink-0 items-center gap-x-2">
        <img class="h-8 w-auto" src="https://tailwindui.com/img/logos/mark.svg?color=indigo&shade=500" alt="Your Company">
        <h1 class="text-white font-semibold text-2xl">emrgnt</h1>
      </div>
      <nav class="flex flex-1 flex-col">
        <ul role="list" class="flex flex-1 flex-col gap-y-7">
          <li>
            <div class="text-xs font-semibold leading-6 text-gray-400">Projects</div>
            <ul role="list" class="-mx-2 mt-2 space-y-1">
              <li>
                <!-- Current: "bg-gray-800 text-white", Default: "text-gray-400 hover:text-white hover:bg-gray-800" -->
                <a href="#" class="bg-gray-800 text-white hover:text-white hover:bg-gray-800 group flex gap-x-3 rounded-md p-2 text-sm leading-6 font-semibold">
                  <span class="truncate">Sample Project</span>
                </a>
              </li>
            </ul>
          </li>
          
          <li class="mt-auto">
            <button type="button" class="-m-1.5 flex items-center p-1.5" id="user-menu-button" aria-expanded="false" aria-haspopup="true">
              <span class="sr-only">Open user menu</span>
              <img class="h-8 w-8 rounded-full bg-gray-50" src="https://media.licdn.com/dms/image/C4E03AQGI68ID-1YJeQ/profile-displayphoto-shrink_800_800/0/1633732741823?e=1710979200&v=beta&t=gxYWv64omC7TNfagDIWB1gHNYlvUWvRJy-eNe1S8cHQ" alt="">
              <span class="hidden lg:flex lg:items-center">
                <span class="ml-4 text-sm leading-6 text-gray-400" aria-hidden="true">Nick Edwards</span>
              </span>
            </button>
          </li>
        </ul>
      </nav>
    </div>
  </div>

        <slot />
</div>

{/if}