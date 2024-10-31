<template>
  <div class="flex w-full h-full items-center justify-center">
    <div class="text-white text-center !text-md">
      <div className="flex flex-col gap-2">
        <div className="bg-purple-500/25 border-2 border-blue-500 p-2">
          Header
        </div>
        <div className="flex gap-2 w-[512px]">
          <div className="flex-[1] bg-neutral-500/25 p-2">
            Sidebar (Static HTML)
          </div>
          <div className="flex-[2] flex flex-col gap-2">
            <div className="h-38 bg-neutral-500/25 p-2">
              Details (Static HTML)
            </div>
            <div className="h-16 bg-purple-500/25 border-2 border-green-500 p-2">
              Image carousel
            </div>
          </div>
        </div>
        <div className="bg-neutral-500/25 p-2 flex-1">
          Footer (Static HTML)
        </div>
      </div>
    </div>
  </div>
</template>