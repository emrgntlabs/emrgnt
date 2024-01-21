<script>
  import "../app.css";
  import { page } from '$app/stores';  

  $: pathname = $page.url.pathname
  $: isKbSelected = pathname == "/kb";

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
                {#if !isKbSelected}
                  <a href="/" class="bg-gray-800 text-white hover:text-white hover:bg-gray-800 group flex gap-x-3 rounded-md p-2 text-sm leading-6 font-semibold">
                    <span class="truncate">Sample Project</span>
                  </a>
                {:else}
                  <a href="/" class="text-gray-400 hover:text-white hover:bg-gray-800 group flex gap-x-3 rounded-md p-2 text-sm leading-6 font-semibold">
                    <span class="truncate">Sample Project</span>
                  </a>
                {/if}
              </li>
            </ul>
          </li>
          <li class="mt-24">
            <ul role="list" class="-mx-2 space-y-1">
              <li>
                {#if isKbSelected}
                  <a href="/kb" class="bg-gray-800 text-white hover:text-white hover:bg-gray-800 group flex gap-x-3 rounded-md p-2 text-sm leading-6 font-semibold">
                    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
                      <path stroke-linecap="round" stroke-linejoin="round" d="M4.26 10.147a60.438 60.438 0 0 0-.491 6.347A48.62 48.62 0 0 1 12 20.904a48.62 48.62 0 0 1 8.232-4.41 60.46 60.46 0 0 0-.491-6.347m-15.482 0a50.636 50.636 0 0 0-2.658-.813A59.906 59.906 0 0 1 12 3.493a59.903 59.903 0 0 1 10.399 5.84c-.896.248-1.783.52-2.658.814m-15.482 0A50.717 50.717 0 0 1 12 13.489a50.702 50.702 0 0 1 7.74-3.342M6.75 15a.75.75 0 1 0 0-1.5.75.75 0 0 0 0 1.5Zm0 0v-3.675A55.378 55.378 0 0 1 12 8.443m-7.007 11.55A5.981 5.981 0 0 0 6.75 15.75v-1.5" />
                    </svg>                
                    <span class="truncate">Knowledge Base</span>
                  </a>
                {:else}
                <a href="/kb" class="text-gray-400 hover:text-white hover:bg-gray-800 group flex gap-x-3 rounded-md p-2 text-sm leading-6 font-semibold">
                  <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M4.26 10.147a60.438 60.438 0 0 0-.491 6.347A48.62 48.62 0 0 1 12 20.904a48.62 48.62 0 0 1 8.232-4.41 60.46 60.46 0 0 0-.491-6.347m-15.482 0a50.636 50.636 0 0 0-2.658-.813A59.906 59.906 0 0 1 12 3.493a59.903 59.903 0 0 1 10.399 5.84c-.896.248-1.783.52-2.658.814m-15.482 0A50.717 50.717 0 0 1 12 13.489a50.702 50.702 0 0 1 7.74-3.342M6.75 15a.75.75 0 1 0 0-1.5.75.75 0 0 0 0 1.5Zm0 0v-3.675A55.378 55.378 0 0 1 12 8.443m-7.007 11.55A5.981 5.981 0 0 0 6.75 15.75v-1.5" />
                  </svg>                
                  <span class="truncate">Knowledge Base</span>
                </a>
                {/if}            
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

  <div class="pl-72">
    <slot />
  </div>
</div>

{/if}