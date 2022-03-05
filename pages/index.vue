<template>
  <div class="editor">
	  <div class="editor-inner">
		  <div class="sidebar">
			  <div class="window-buttons">
				  <div class="circle circle-red"></div>
				  <div class="circle circle-yellow"></div>
				  <div class="circle circle-green"></div>
			  </div>
			  <div class="file-explorer">
				  <h2>File Explorer</h2>
			  </div>
		  </div>
		  <div class="file-editor">
			  <div class="file-editor-tabs">
				  <div class="file-editor-tab">
					  <span>icon</span>
					  <span>index.md</span>
				  </div>
				  <div class="file-editor-tab">
					  <span>icon</span>
					  <span>about.md</span>
				  </div>
			  </div>
			  <div class="file-editor-window">
				  <div class="file-editor-numbers">
						<span v-for="n in 22" :key="n">{{ n }} </span>
				  </div>
				  <div class="file-editor-lines">
					  <span class="file-editor-line file-editor-comment">// Titel der Seite</span>
					  <span class="file-editor-line file-editor-line-md"> # tommycodes.site</span>
					  <span class="file-editor-line file-editor-comment">// Information über den Author</span>
					  <span class="file-editor-line file-editor-line-md">## About me</span>
					  <span class="file-editor-line">
						  I'm a software developer  from  Bielefeld, Germany.
					  </span>
				  </div>
			  </div>
		  </div>

	  </div>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
}
</script>

<style scoped>
.editor{
	background: var(--editor-bg);
	margin: auto;
	border-radius: 10px;
	box-shadow: 0 1px 4px rgba(0, 0, 0, 0.3);
}
.editor-inner{
	padding: 5px;
	display: grid;
	grid-template-columns: 200px 1fr;
	height: calc(100vh - 50px);

}

.sidebar{
	display: flex;
	flex-direction: column;
	padding: 15px;
}

.sidebar h2{
	opacity: 0.6;
	font-size: 1.2em;
}

.window-buttons{
	display: flex;
	margin: 0 0 10px 0;
}
.circle{
	height: 10px;
	width: 10px;
	border-radius: 50%;
	margin-right: 7.5px;
}

.circle-red{
	background: red;
}
.circle-yellow{
	background: yellow;
}
.circle-green{
	background: green;
}

.file-editor{
	background: var(--file-editor);
	border-top-right-radius: 10px;
	padding-left: 25px;
	padding-top: 10px;
}
.file-editor-tabs{
	display: flex;
}
.file-editor-tab{
	margin-right: 20px;
	opacity: 0.6;
}
.file-editor-window{
	display: flex;
	margin-top: 15px;
}
.file-editor-numbers, .file-editor-lines{
	display: flex;
	flex-direction: column;
}
.file-editor-numbers{
	margin-right: 15px;
}
.file-editor-numbers >span, .file-editor-lines > span{
	opacity: 0.4;
	margin-bottom: 5px;
	font-size: .8em;
}
.file-editor-lines{
	flex-grow: 1;
}
.file-editor-lines > span {
	opacity: 1;
	color: #fff;
}

.file-editor-lines .file-editor-line-md{
	color: var(--primary-color);
}

.file-editor-lines .file-editor-comment{
	color: var(--secondary-color);
	font-style: italic;
}
</style>