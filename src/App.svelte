<script>
  import logo from "./assets/svelte.png";
  import Counter from "./lib/Counter.svelte";
  import NuevaSolicitud from "./lib/NuevaSolicitud.svelte";
  import SolicitudesPage from "./lib/SolicitudesPage.svelte";
  let paginaActual = "SOLICITUDES";
</script>

<main>
  <ion-app>
    <ion-header translucent>
      <ion-toolbar>
        <ion-title>Esperando autorización</ion-title>
      </ion-toolbar>
    </ion-header>

    {#if paginaActual == "SOLICITUDES"}
      <SolicitudesPage
        on:nueva_solicitud={() => (paginaActual = "NUEVA_SOLICITUD")}
      />
    {/if}
    {#if paginaActual == "NUEVA_SOLICITUD"}
      <NuevaSolicitud
        on:aceptar={() => (paginaActual = "SOLICITUDES")}
        on:cancelar={() => (paginaActual = "SOLICITUDES")}
      />
    {/if}
  </ion-app>
</main>
