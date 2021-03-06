<template>
    <div>
        <GalleriaSubMenu />

        <div class="content-section introduction">
            <div class="feature-intro">
                <h1 style="margin-bottom: 0px;">Galleria - Preview</h1>
                <p></p>
            </div>
        </div>

        <div class="content-section implementation">
            <h3 class="first">Basic</h3>
            <Galleria :value="images" :responsiveOptions="responsiveOptions" :numVisible="5" :circular="true" style="max-width: 520px">
                <template #item="slotProps">
					<img :src="slotProps.item.previewImageSrc" :alt="slotProps.item.alt" style="width: 100%; display: block;" />
				</template>
				<template #thumbnail="slotProps">
                    <div class="p-grid p-nogutter p-justify-center">
                        <img :src="slotProps.item.thumbnailImageSrc" :alt="slotProps.item.alt" style="display: block;" />
                    </div>
				</template>
            </Galleria>

            <h3>Navigation Buttons</h3>
            <Galleria :value="images" :responsiveOptions="responsiveOptions" :numVisible="5" :circular="true" style="max-width: 520px"
                :showPreviewNavButtons="true">
                <template #header>
                    With Thumbnails
                </template>
                <template #item="slotProps">
					<img :src="slotProps.item.previewImageSrc" :alt="slotProps.item.alt" style="width: 100%; display: block;" />
				</template>
				<template #thumbnail="slotProps">
                    <div class="p-grid p-nogutter p-justify-center">
                        <img :src="slotProps.item.thumbnailImageSrc" :alt="slotProps.item.alt" style="display: block;" />
                    </div>
				</template>
            </Galleria>

            <Galleria :value="images" :responsiveOptions="responsiveOptions" :numVisible="5" :circular="true" style="max-width: 520px; margin-top: 2em"
                :showPreviewNavButtons="true" :showThumbnails="false">
                <template #header>
                    Without Thumbnails
                </template>
                <template #item="slotProps">
					<img :src="slotProps.item.previewImageSrc" :alt="slotProps.item.alt" style="width: 100%; display: block;" />
				</template>
				<template #thumbnail="slotProps">
                    <div class="p-grid p-nogutter p-justify-center">
                        <img :src="slotProps.item.thumbnailImageSrc" :alt="slotProps.item.alt" style="display: block;" />
                    </div>
				</template>
            </Galleria>

            <h3>Show Navigation Buttons on Preview Hover</h3>
            <Galleria :value="images" :responsiveOptions="responsiveOptions" :numVisible="5" :circular="true" style="max-width: 520px;"
                :showPreviewNavButtons="true" :showNavButtonsOnPreviewHover="true">
                <template #header>
                    With Thumbnails
                </template>
                <template #item="slotProps">
					<img :src="slotProps.item.previewImageSrc" :alt="slotProps.item.alt" style="width: 100%; display: block;" />
				</template>
				<template #thumbnail="slotProps">
                    <div class="p-grid p-nogutter p-justify-center">
                        <img :src="slotProps.item.thumbnailImageSrc" :alt="slotProps.item.alt" style="display: block;" />
                    </div>
				</template>
            </Galleria>

            <Galleria :value="images" :responsiveOptions="responsiveOptions" :numVisible="5" :circular="true" style="max-width: 520px; margin-top: 2em"
                :showPreviewNavButtons="true" :showThumbnails="false" :showNavButtonsOnPreviewHover="true">
                <template #header>
                    Without Thumbnails
                </template>
                <template #item="slotProps">
					<img :src="slotProps.item.previewImageSrc" :alt="slotProps.item.alt" style="width: 100%; display: block;" />
				</template>
				<template #thumbnail="slotProps">
                    <div class="p-grid p-nogutter p-justify-center">
                        <img :src="slotProps.item.thumbnailImageSrc" :alt="slotProps.item.alt" style="display: block;" />
                    </div>
				</template>
            </Galleria>

            <h3>Advanced</h3>
            <Galleria :value="images" :responsiveOptions="responsiveOptions" :numVisible="5" :circular="true" style="max-width: 520px;"
                :showPreviewNavButtons="true" :showThumbnails="false" :showNavButtonsOnPreviewHover="true"
                :showIndicators="true" :showIndicatorsOnPreview="true" :changePreviewOnIndicatorHover="true">
                <template #item="slotProps">
					<img :src="slotProps.item.previewImageSrc" :alt="slotProps.item.alt" style="width: 100%; display: block;" />
				</template>
				<template #thumbnail="slotProps">
                    <div class="p-grid p-nogutter p-justify-center">
                        <img :src="slotProps.item.thumbnailImageSrc" :alt="slotProps.item.alt" style="display: block;" />
                    </div>
				</template>
            </Galleria>
        </div>

        <div class="content-section documentation">
            <TabView>
                <TabPanel header="Source">
<CodeHighlight>
<template v-pre>
&lt;h3 class="first"&gt;Basic&lt;/h3&gt;
&lt;Galleria :value="images" :responsiveOptions="responsiveOptions" :numVisible="5" :circular="true" style="max-width: 520px"&gt;
    &lt;template #item="slotProps"&gt;
        &lt;img :src="slotProps.item.previewImageSrc" :alt="slotProps.item.alt" style="width: 100%; display: block;" /&gt;
    &lt;/template&gt;
    &lt;template #thumbnail="slotProps"&gt;
        &lt;div class="p-grid p-nogutter p-justify-center"&gt;
            &lt;img :src="slotProps.item.thumbnailImageSrc" :alt="slotProps.item.alt" style="display: block;" /&gt;
        &lt;/div&gt;
    &lt;/template&gt;
&lt;/Galleria&gt;

&lt;h3&gt;Navigation Buttons&lt;/h3&gt;
&lt;Galleria :value="images" :responsiveOptions="responsiveOptions" :numVisible="5" :circular="true" style="max-width: 520px"
    :showPreviewNavButtons="true"&gt;
    &lt;template #header&gt;
        With Thumbnails
    &lt;/template&gt;
    &lt;template #item="slotProps"&gt;
        &lt;img :src="slotProps.item.previewImageSrc" :alt="slotProps.item.alt" style="width: 100%; display: block;" /&gt;
    &lt;/template&gt;
    &lt;template #thumbnail="slotProps"&gt;
        &lt;div class="p-grid p-nogutter p-justify-center"&gt;
            &lt;img :src="slotProps.item.thumbnailImageSrc" :alt="slotProps.item.alt" style="display: block;" /&gt;
        &lt;/div&gt;
    &lt;/template&gt;
&lt;/Galleria&gt;

&lt;Galleria :value="images" :responsiveOptions="responsiveOptions" :numVisible="5" :circular="true" style="max-width: 520px; margin-top: 2em"
    :showPreviewNavButtons="true" :showThumbnails="false"&gt;
    &lt;template #header&gt;
        Without Thumbnails
    &lt;/template&gt;
    &lt;template #item="slotProps"&gt;
        &lt;img :src="slotProps.item.previewImageSrc" :alt="slotProps.item.alt" style="width: 100%; display: block;" /&gt;
    &lt;/template&gt;
    &lt;template #thumbnail="slotProps"&gt;
        &lt;div class="p-grid p-nogutter p-justify-center"&gt;
            &lt;img :src="slotProps.item.thumbnailImageSrc" :alt="slotProps.item.alt" style="display: block;" /&gt;
        &lt;/div&gt;
    &lt;/template&gt;
&lt;/Galleria&gt;

&lt;h3&gt;Show Navigation Buttons on Preview Hover&lt;/h3&gt;
&lt;Galleria :value="images" :responsiveOptions="responsiveOptions" :numVisible="5" :circular="true" style="max-width: 520px;"
    :showPreviewNavButtons="true" :showNavButtonsOnPreviewHover="true"&gt;
    &lt;template #header&gt;
        With Thumbnails
    &lt;/template&gt;
    &lt;template #item="slotProps"&gt;
        &lt;img :src="slotProps.item.previewImageSrc" :alt="slotProps.item.alt" style="width: 100%; display: block;" /&gt;
    &lt;/template&gt;
    &lt;template #thumbnail="slotProps"&gt;
        &lt;div class="p-grid p-nogutter p-justify-center"&gt;
            &lt;img :src="slotProps.item.thumbnailImageSrc" :alt="slotProps.item.alt" style="display: block;" /&gt;
        &lt;/div&gt;
    &lt;/template&gt;
&lt;/Galleria&gt;

&lt;Galleria :value="images" :responsiveOptions="responsiveOptions" :numVisible="5" :circular="true" style="max-width: 520px; margin-top: 2em"
    :showPreviewNavButtons="true" :showThumbnails="false" :showNavButtonsOnPreviewHover="true"&gt;
    &lt;template #header&gt;
        Without Thumbnails
    &lt;/template&gt;
    &lt;template #item="slotProps"&gt;
        &lt;img :src="slotProps.item.previewImageSrc" :alt="slotProps.item.alt" style="width: 100%; display: block;" /&gt;
    &lt;/template&gt;
    &lt;template #thumbnail="slotProps"&gt;
        &lt;div class="p-grid p-nogutter p-justify-center"&gt;
            &lt;img :src="slotProps.item.thumbnailImageSrc" :alt="slotProps.item.alt" style="display: block;" /&gt;
        &lt;/div&gt;
    &lt;/template&gt;
&lt;/Galleria&gt;

&lt;h3&gt;Advanced&lt;/h3&gt;
&lt;Galleria :value="images" :responsiveOptions="responsiveOptions" :numVisible="5" :circular="true" style="max-width: 520px;"
    :showPreviewNavButtons="true" :showThumbnails="false" :showNavButtonsOnPreviewHover="true"
    :showIndicators="true" :showIndicatorsOnPreview="true" :changePreviewOnIndicatorHover="true"&gt;
    &lt;template #item="slotProps"&gt;
        &lt;img :src="slotProps.item.previewImageSrc" :alt="slotProps.item.alt" style="width: 100%; display: block;" /&gt;
    &lt;/template&gt;
    &lt;template #thumbnail="slotProps"&gt;
        &lt;div class="p-grid p-nogutter p-justify-center"&gt;
            &lt;img :src="slotProps.item.thumbnailImageSrc" :alt="slotProps.item.alt" style="display: block;" /&gt;
        &lt;/div&gt;
    &lt;/template&gt;
&lt;/Galleria&gt;
</template>
</CodeHighlight>

<CodeHighlight lang="javascript">
import GalleriaService from '../../service/GalleriaService';

export default {
    data() {
        return {
            images: null,
			responsiveOptions: [
				{
                    breakpoint: '1024px',
                    numVisible: 5
                },
                {
                    breakpoint: '768px',
                    numVisible: 3
                },
                {
                    breakpoint: '560px',
                    numVisible: 1
                }
			]
        }
    },
    galleriaService: null,
	created() {
		this.galleriaService = new GalleriaService();
	},
	mounted() {
		this.galleriaService.getImages().then(data => this.images = data);
    }
}
</CodeHighlight>
                </TabPanel>
            </TabView>
        </div>
    </div>
</template>

<script>
import GalleriaService from '../../service/GalleriaService';
import GalleriaSubMenu from './GalleriaSubMenu';

export default {
    data() {
        return {
            images: null,
			responsiveOptions: [
				{
                    breakpoint: '1024px',
                    numVisible: 5
                },
                {
                    breakpoint: '768px',
                    numVisible: 3
                },
                {
                    breakpoint: '560px',
                    numVisible: 1
                }
			]
        }
    },
    galleriaService: null,
	created() {
		this.galleriaService = new GalleriaService();
	},
	mounted() {
		this.galleriaService.getImages().then(data => this.images = data);
    },
    components: {
        'GalleriaSubMenu': GalleriaSubMenu
    }
}
</script>
