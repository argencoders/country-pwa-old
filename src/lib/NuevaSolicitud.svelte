<script>
import { createEventDispatcher } from "svelte";

const dispatch = createEventDispatcher();

function aceptar() {
    dispatch("aceptar");
}
function cancelar() {
    dispatch("cancelar");
}
</script>

<ion-content fullscreen>
    Nueva solicitud
    <ion-button color="primary" on:click={aceptar}>Aceptar</ion-button>
    <ion-button color="danger" on:click={cancelar}>Cancelar</ion-button>
</ion-content>