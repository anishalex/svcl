<!-- src/routes/about.svelte -->
<script>
    import ImageGallery from './ImageGallery.svelte';
    const postBody = "FIRM PRICE, PICK UP\n\nHP Pavilion Gaming Laptop 15-dk1010ca\n• Windows 10 Home 64-Bit\n• 10th Generation Intel Core i5-10300H 2.5Ghz Quad (4.5Ghz Max Turbo)\n• 15.6-inch diagonal FHD 1920x1080, IPS, anti-glare, micro-edge, WLED-backlit\n• 8 GB DDR4 RAM\n• 256 GB PCIe NVMe M.2 SSD\n• NVIDIA GeForce GTX 1050 (3 GB GDDR5 dedicated), Intel UHD Graphics\n• Audio by Bang and Olufsen with dual speakers\n• Intel Wi-Fi 6 AX 201 (2x2) and Bluetooth 5 combo, MU-MIMO supported\n• HDMI, USB-C, USB 3.0, USB 2.0, Ethernet, headphone jack, memory card reader\n• 3-cell Lithium Ion 52.5 Wh with HP SmartCharge\n• HP Wide Vision 720p HD Camera with integrated dual array digital microphone\n• Product weight: 4.92 lb\n\nThe laptop is used, in excellent (like new) condition\n\nIt comes with the original box and manuals, original HP 135w smart charger, full MS Office\n\nUnder HP Warranty until end of March 2022\n\nRetails for $1130 after tax at walmart, amazon\n\nhttps://www.walmart.ca/en/ip/hp-pavilion-gaming-laptop-15-dk1010ca-intel-core-i5-10300h10m25uaabl-shadow-black/6000201797937\n\nhttps://www.amazon.ca/HP-Pavilion-15-dk1010ca-i5-10300H-GeForce/dp/B087J6HC73\n\nTags: Alienware HP Omen Acer Predator Dell XPS Gaming Laptop Lenovo Legion Asus Rog Strix Asus Rog Zephyrus Acer Nitro Razer Blade"
          
</script>

<style>
  .bodytext {
    white-space: pre-line
 }
</style>

<svelte:head>
	<title>Specific Post</title>
</svelte:head>

<div class="flex flex-wrap overflow-hidden">

    <div class="w-full overflow-hidden lg:w-3/4 xl:w-3/4">
      <h1 class="font-bold">Product Main Title Goes here</h1>
      <ImageGallery />
      <p class="bodytext m-12">{postBody}</p>

    </div>
  
    <div class="w-full bg-yellow-400 overflow-hidden lg:w-1/4 xl:w-1/4">
      <!-- Column Content -->
      <p>Map if required goes here</p>
    </div>
  
    <div class="w-full bg-green-400 overflow-hidden lg:w-1/2 xl:w-1/2">
      <!-- Column Content -->
      <p>Description and body content here</p>
      <p>Contact and visible metadata here</p>
    </div>
  
    <div class="w-full bg-blue-400 overflow-hidden lg:w-1/2 xl:w-1/2">
      <!-- Column Content -->
      <p>Spacer block - keep this empty in production</p>
    </div>
  
  </div>