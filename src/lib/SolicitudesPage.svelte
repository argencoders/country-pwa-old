<script>
    import { createEventDispatcher } from "svelte";

    const dispatch = createEventDispatcher();

    function nuevaSolicitud() {
        dispatch("nueva_solicitud");
    }
</script>

<ion-content fullscreen>
    <ion-list>
        <ion-list-header> Solicitudes </ion-list-header>

        <ion-item>
            <ion-avatar slot="start">
                <!-- svelte-ignore a11y-missing-attribute -->
                <img src="./img/man-1.png" />
            </ion-avatar>
            <ion-label>
                <h2>Peky Diaz</h2>
                <h3>Instalador de aire</h3>
                <ion-button color="warning">22</ion-button>
            </ion-label>
        </ion-item>

        <ion-item>
            <ion-avatar slot="start">
                <!-- svelte-ignore a11y-missing-attribute -->
                <img src="./img/man-2.png" />
            </ion-avatar>
            <ion-label>
                <h2>Juan Gonzalez</h2>
                <h3>Plomero</h3>
                <ion-button color="warning">6</ion-button>
            </ion-label>
        </ion-item>

        <ion-item>
            <ion-avatar slot="start">
                <!-- svelte-ignore a11y-missing-attribute -->
                <img src="./img/woman-1.png" />
            </ion-avatar>
            <ion-label>
                <h2>Maria Rosa Ramirez</h2>
                <h3>Limpieza</h3>
                <ion-button color="warning">14</ion-button>
            </ion-label>
        </ion-item>
    </ion-list>

    <ion-fab vertical="bottom" horizontal="end" slot="fixed">
        <ion-fab-button on:click={() => nuevaSolicitud()}>
            <ion-icon name="add" />
        </ion-fab-button>
    </ion-fab>
</ion-content>
