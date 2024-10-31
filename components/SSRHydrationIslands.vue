<template>
  <div class="flex w-full h-full items-center">
    <div className="flex gap-4 text-white text-center !text-sm">
      <div className="flex-1 space-y-4">
        <h2 className="!text-xl font-bold">
          SSR
        </h2>
        <div className="flex flex-col gap-2">
          <div className="bg-purple-500/25 border-2 border-blue-500 p-2">
            Header
          </div>
          <div className="flex gap-2">
            <div className="flex-[1] bg-neutral-500/25 border-2 border-blue-500 p-2">
              Sidebar
            </div>
            <div className="flex-[2] flex flex-col gap-2">
              <div className="h-24 bg-neutral-500/25 border-2 border-blue-500 p-2">
                Details
              </div>
              <div className="bg-purple-500/25 border-2 border-blue-500 p-2">
                Image carousel
              </div>
            </div>
          </div>
          <div className="bg-neutral-500/25 border-2 border-blue-500 p-2 flex-1">
            Footer
          </div>
        </div>
        <p className="text-md">
          (Pré-)Rendu côté serveur + réhydratation côté client
        </p>
      </div>

      <div className="flex-1 space-y-4">
        <h2 className="!text-xl font-bold">
          Progressive Hydration
        </h2>
        <div className="flex flex-col gap-2">
          <div className="bg-purple-500/25 border-2 border-blue-500 p-2">
            Header
          </div>
          <div className="flex gap-2">
            <div className="flex-[1] bg-neutral-500/25 border-2 border-blue-500 p-2">
              Sidebar
            </div>
            <div className="flex-[2] flex flex-col gap-2">
              <div className="h-24 bg-neutral-500/25 border-2 border-blue-500 p-2">
                Details
              </div>
              <div className="bg-purple-500/25 border-2 border-green-500 p-2">
                Image carousel
              </div>
            </div>
          </div>
          <div className="bg-neutral-500/25 border-2 border-blue-500 p-2 flex-1">
            Footer
          </div>
        </div>
        <p className="text-md">
          (Pré-)Rendû côté serveur + réhydratation côté client prioritaire puis progressif
        </p>
      </div>

      <div className="flex-1 space-y-4">
        <h2 className="!text-xl font-bold">
          Islands
        </h2>
        <div className="flex flex-col gap-2">
          <div className="bg-purple-500/25 border-2 border-yellow-500 p-2">
            Header
          </div>
          <div className="flex gap-2">
            <div className="flex-[1] bg-purple-500/25 border-2 border-yellow-500 p-2">
              Sidebar
            </div>
            <div className="flex-[2] flex flex-col gap-2">
              <div className="h-24 bg-neutral-500/25 border-2 border-transparent p-2">
                Details
              </div>
              <div className="bg-purple-500/25 p-2 border-2 border-yellow-500">
                Image carousel
              </div>
            </div>
          </div>
          <div className="bg-neutral-500/25 p-2 border-2 border-transparent flex-1">
            Footer
          </div>
        </div>
        <p className="text-md">
          (Pré-)Rendu côté serveur + chargement des scripts si nécessaires
        </p>
      </div>
    </div>
  </div>
</template>