<!DOCTYPE html>
<html>
<head><meta charset="utf-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Project</title><script src="https://cdnjs.cloudflare.com/ajax/libs/require.js/2.1.10/require.min.js"></script>




<style type="text/css">
    pre { line-height: 125%; }
td.linenos .normal { color: inherit; background-color: transparent; padding-left: 5px; padding-right: 5px; }
span.linenos { color: inherit; background-color: transparent; padding-left: 5px; padding-right: 5px; }
td.linenos .special { color: #000000; background-color: #ffffc0; padding-left: 5px; padding-right: 5px; }
span.linenos.special { color: #000000; background-color: #ffffc0; padding-left: 5px; padding-right: 5px; }
.highlight .hll { background-color: var(--jp-cell-editor-active-background) }
.highlight { background: var(--jp-cell-editor-background); color: var(--jp-mirror-editor-variable-color) }
.highlight .c { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment */
.highlight .err { color: var(--jp-mirror-editor-error-color) } /* Error */
.highlight .k { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword */
.highlight .o { color: var(--jp-mirror-editor-operator-color); font-weight: bold } /* Operator */
.highlight .p { color: var(--jp-mirror-editor-punctuation-color) } /* Punctuation */
.highlight .ch { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.Hashbang */
.highlight .cm { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.Multiline */
.highlight .cp { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.Preproc */
.highlight .cpf { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.PreprocFile */
.highlight .c1 { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.Single */
.highlight .cs { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.Special */
.highlight .kc { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Constant */
.highlight .kd { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Declaration */
.highlight .kn { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Namespace */
.highlight .kp { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Pseudo */
.highlight .kr { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Reserved */
.highlight .kt { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Type */
.highlight .m { color: var(--jp-mirror-editor-number-color) } /* Literal.Number */
.highlight .s { color: var(--jp-mirror-editor-string-color) } /* Literal.String */
.highlight .ow { color: var(--jp-mirror-editor-operator-color); font-weight: bold } /* Operator.Word */
.highlight .pm { color: var(--jp-mirror-editor-punctuation-color) } /* Punctuation.Marker */
.highlight .w { color: var(--jp-mirror-editor-variable-color) } /* Text.Whitespace */
.highlight .mb { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Bin */
.highlight .mf { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Float */
.highlight .mh { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Hex */
.highlight .mi { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Integer */
.highlight .mo { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Oct */
.highlight .sa { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Affix */
.highlight .sb { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Backtick */
.highlight .sc { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Char */
.highlight .dl { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Delimiter */
.highlight .sd { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Doc */
.highlight .s2 { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Double */
.highlight .se { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Escape */
.highlight .sh { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Heredoc */
.highlight .si { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Interpol */
.highlight .sx { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Other */
.highlight .sr { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Regex */
.highlight .s1 { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Single */
.highlight .ss { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Symbol */
.highlight .il { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Integer.Long */
  </style>



<style type="text/css">
/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*
 * Mozilla scrollbar styling
 */

/* use standard opaque scrollbars for most nodes */
[data-jp-theme-scrollbars='true'] {
  scrollbar-color: rgb(var(--jp-scrollbar-thumb-color))
    var(--jp-scrollbar-background-color);
}

/* for code nodes, use a transparent style of scrollbar. These selectors
 * will match lower in the tree, and so will override the above */
[data-jp-theme-scrollbars='true'] .CodeMirror-hscrollbar,
[data-jp-theme-scrollbars='true'] .CodeMirror-vscrollbar {
  scrollbar-color: rgba(var(--jp-scrollbar-thumb-color), 0.5) transparent;
}

/* tiny scrollbar */

.jp-scrollbar-tiny {
  scrollbar-color: rgba(var(--jp-scrollbar-thumb-color), 0.5) transparent;
  scrollbar-width: thin;
}

/*
 * Webkit scrollbar styling
 */

/* use standard opaque scrollbars for most nodes */

[data-jp-theme-scrollbars='true'] ::-webkit-scrollbar,
[data-jp-theme-scrollbars='true'] ::-webkit-scrollbar-corner {
  background: var(--jp-scrollbar-background-color);
}

[data-jp-theme-scrollbars='true'] ::-webkit-scrollbar-thumb {
  background: rgb(var(--jp-scrollbar-thumb-color));
  border: var(--jp-scrollbar-thumb-margin) solid transparent;
  background-clip: content-box;
  border-radius: var(--jp-scrollbar-thumb-radius);
}

[data-jp-theme-scrollbars='true'] ::-webkit-scrollbar-track:horizontal {
  border-left: var(--jp-scrollbar-endpad) solid
    var(--jp-scrollbar-background-color);
  border-right: var(--jp-scrollbar-endpad) solid
    var(--jp-scrollbar-background-color);
}

[data-jp-theme-scrollbars='true'] ::-webkit-scrollbar-track:vertical {
  border-top: var(--jp-scrollbar-endpad) solid
    var(--jp-scrollbar-background-color);
  border-bottom: var(--jp-scrollbar-endpad) solid
    var(--jp-scrollbar-background-color);
}

/* for code nodes, use a transparent style of scrollbar */

[data-jp-theme-scrollbars='true'] .CodeMirror-hscrollbar::-webkit-scrollbar,
[data-jp-theme-scrollbars='true'] .CodeMirror-vscrollbar::-webkit-scrollbar,
[data-jp-theme-scrollbars='true']
  .CodeMirror-hscrollbar::-webkit-scrollbar-corner,
[data-jp-theme-scrollbars='true']
  .CodeMirror-vscrollbar::-webkit-scrollbar-corner {
  background-color: transparent;
}

[data-jp-theme-scrollbars='true']
  .CodeMirror-hscrollbar::-webkit-scrollbar-thumb,
[data-jp-theme-scrollbars='true']
  .CodeMirror-vscrollbar::-webkit-scrollbar-thumb {
  background: rgba(var(--jp-scrollbar-thumb-color), 0.5);
  border: var(--jp-scrollbar-thumb-margin) solid transparent;
  background-clip: content-box;
  border-radius: var(--jp-scrollbar-thumb-radius);
}

[data-jp-theme-scrollbars='true']
  .CodeMirror-hscrollbar::-webkit-scrollbar-track:horizontal {
  border-left: var(--jp-scrollbar-endpad) solid transparent;
  border-right: var(--jp-scrollbar-endpad) solid transparent;
}

[data-jp-theme-scrollbars='true']
  .CodeMirror-vscrollbar::-webkit-scrollbar-track:vertical {
  border-top: var(--jp-scrollbar-endpad) solid transparent;
  border-bottom: var(--jp-scrollbar-endpad) solid transparent;
}

/* tiny scrollbar */

.jp-scrollbar-tiny::-webkit-scrollbar,
.jp-scrollbar-tiny::-webkit-scrollbar-corner {
  background-color: transparent;
  height: 4px;
  width: 4px;
}

.jp-scrollbar-tiny::-webkit-scrollbar-thumb {
  background: rgba(var(--jp-scrollbar-thumb-color), 0.5);
}

.jp-scrollbar-tiny::-webkit-scrollbar-track:horizontal {
  border-left: 0px solid transparent;
  border-right: 0px solid transparent;
}

.jp-scrollbar-tiny::-webkit-scrollbar-track:vertical {
  border-top: 0px solid transparent;
  border-bottom: 0px solid transparent;
}

/*
 * Phosphor
 */

.lm-ScrollBar[data-orientation='horizontal'] {
  min-height: 16px;
  max-height: 16px;
  min-width: 45px;
  border-top: 1px solid #a0a0a0;
}

.lm-ScrollBar[data-orientation='vertical'] {
  min-width: 16px;
  max-width: 16px;
  min-height: 45px;
  border-left: 1px solid #a0a0a0;
}

.lm-ScrollBar-button {
  background-color: #f0f0f0;
  background-position: center center;
  min-height: 15px;
  max-height: 15px;
  min-width: 15px;
  max-width: 15px;
}

.lm-ScrollBar-button:hover {
  background-color: #dadada;
}

.lm-ScrollBar-button.lm-mod-active {
  background-color: #cdcdcd;
}

.lm-ScrollBar-track {
  background: #f0f0f0;
}

.lm-ScrollBar-thumb {
  background: #cdcdcd;
}

.lm-ScrollBar-thumb:hover {
  background: #bababa;
}

.lm-ScrollBar-thumb.lm-mod-active {
  background: #a0a0a0;
}

.lm-ScrollBar[data-orientation='horizontal'] .lm-ScrollBar-thumb {
  height: 100%;
  min-width: 15px;
  border-left: 1px solid #a0a0a0;
  border-right: 1px solid #a0a0a0;
}

.lm-ScrollBar[data-orientation='vertical'] .lm-ScrollBar-thumb {
  width: 100%;
  min-height: 15px;
  border-top: 1px solid #a0a0a0;
  border-bottom: 1px solid #a0a0a0;
}

.lm-ScrollBar[data-orientation='horizontal']
  .lm-ScrollBar-button[data-action='decrement'] {
  background-image: var(--jp-icon-caret-left);
  background-size: 17px;
}

.lm-ScrollBar[data-orientation='horizontal']
  .lm-ScrollBar-button[data-action='increment'] {
  background-image: var(--jp-icon-caret-right);
  background-size: 17px;
}

.lm-ScrollBar[data-orientation='vertical']
  .lm-ScrollBar-button[data-action='decrement'] {
  background-image: var(--jp-icon-caret-up);
  background-size: 17px;
}

.lm-ScrollBar[data-orientation='vertical']
  .lm-ScrollBar-button[data-action='increment'] {
  background-image: var(--jp-icon-caret-down);
  background-size: 17px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-Widget, /* </DEPRECATED> */
.lm-Widget {
  box-sizing: border-box;
  position: relative;
  overflow: hidden;
  cursor: default;
}


/* <DEPRECATED> */ .p-Widget.p-mod-hidden, /* </DEPRECATED> */
.lm-Widget.lm-mod-hidden {
  display: none !important;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-CommandPalette, /* </DEPRECATED> */
.lm-CommandPalette {
  display: flex;
  flex-direction: column;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}


/* <DEPRECATED> */ .p-CommandPalette-search, /* </DEPRECATED> */
.lm-CommandPalette-search {
  flex: 0 0 auto;
}


/* <DEPRECATED> */ .p-CommandPalette-content, /* </DEPRECATED> */
.lm-CommandPalette-content {
  flex: 1 1 auto;
  margin: 0;
  padding: 0;
  min-height: 0;
  overflow: auto;
  list-style-type: none;
}


/* <DEPRECATED> */ .p-CommandPalette-header, /* </DEPRECATED> */
.lm-CommandPalette-header {
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
}


/* <DEPRECATED> */ .p-CommandPalette-item, /* </DEPRECATED> */
.lm-CommandPalette-item {
  display: flex;
  flex-direction: row;
}


/* <DEPRECATED> */ .p-CommandPalette-itemIcon, /* </DEPRECATED> */
.lm-CommandPalette-itemIcon {
  flex: 0 0 auto;
}


/* <DEPRECATED> */ .p-CommandPalette-itemContent, /* </DEPRECATED> */
.lm-CommandPalette-itemContent {
  flex: 1 1 auto;
  overflow: hidden;
}


/* <DEPRECATED> */ .p-CommandPalette-itemShortcut, /* </DEPRECATED> */
.lm-CommandPalette-itemShortcut {
  flex: 0 0 auto;
}


/* <DEPRECATED> */ .p-CommandPalette-itemLabel, /* </DEPRECATED> */
.lm-CommandPalette-itemLabel {
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
}

.lm-close-icon {
	border:1px solid transparent;
  background-color: transparent;
  position: absolute;
	z-index:1;
	right:3%;
	top: 0;
	bottom: 0;
	margin: auto;
	padding: 7px 0;
	display: none;
	vertical-align: middle;
  outline: 0;
  cursor: pointer;
}
.lm-close-icon:after {
	content: "X";
	display: block;
	width: 15px;
	height: 15px;
	text-align: center;
	color:#000;
	font-weight: normal;
	font-size: 12px;
	cursor: pointer;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-DockPanel, /* </DEPRECATED> */
.lm-DockPanel {
  z-index: 0;
}


/* <DEPRECATED> */ .p-DockPanel-widget, /* </DEPRECATED> */
.lm-DockPanel-widget {
  z-index: 0;
}


/* <DEPRECATED> */ .p-DockPanel-tabBar, /* </DEPRECATED> */
.lm-DockPanel-tabBar {
  z-index: 1;
}


/* <DEPRECATED> */ .p-DockPanel-handle, /* </DEPRECATED> */
.lm-DockPanel-handle {
  z-index: 2;
}


/* <DEPRECATED> */ .p-DockPanel-handle.p-mod-hidden, /* </DEPRECATED> */
.lm-DockPanel-handle.lm-mod-hidden {
  display: none !important;
}


/* <DEPRECATED> */ .p-DockPanel-handle:after, /* </DEPRECATED> */
.lm-DockPanel-handle:after {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  content: '';
}


/* <DEPRECATED> */
.p-DockPanel-handle[data-orientation='horizontal'],
/* </DEPRECATED> */
.lm-DockPanel-handle[data-orientation='horizontal'] {
  cursor: ew-resize;
}


/* <DEPRECATED> */
.p-DockPanel-handle[data-orientation='vertical'],
/* </DEPRECATED> */
.lm-DockPanel-handle[data-orientation='vertical'] {
  cursor: ns-resize;
}


/* <DEPRECATED> */
.p-DockPanel-handle[data-orientation='horizontal']:after,
/* </DEPRECATED> */
.lm-DockPanel-handle[data-orientation='horizontal']:after {
  left: 50%;
  min-width: 8px;
  transform: translateX(-50%);
}


/* <DEPRECATED> */
.p-DockPanel-handle[data-orientation='vertical']:after,
/* </DEPRECATED> */
.lm-DockPanel-handle[data-orientation='vertical']:after {
  top: 50%;
  min-height: 8px;
  transform: translateY(-50%);
}


/* <DEPRECATED> */ .p-DockPanel-overlay, /* </DEPRECATED> */
.lm-DockPanel-overlay {
  z-index: 3;
  box-sizing: border-box;
  pointer-events: none;
}


/* <DEPRECATED> */ .p-DockPanel-overlay.p-mod-hidden, /* </DEPRECATED> */
.lm-DockPanel-overlay.lm-mod-hidden {
  display: none !important;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-Menu, /* </DEPRECATED> */
.lm-Menu {
  z-index: 10000;
  position: absolute;
  white-space: nowrap;
  overflow-x: hidden;
  overflow-y: auto;
  outline: none;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}


/* <DEPRECATED> */ .p-Menu-content, /* </DEPRECATED> */
.lm-Menu-content {
  margin: 0;
  padding: 0;
  display: table;
  list-style-type: none;
}


/* <DEPRECATED> */ .p-Menu-item, /* </DEPRECATED> */
.lm-Menu-item {
  display: table-row;
}


/* <DEPRECATED> */
.p-Menu-item.p-mod-hidden,
.p-Menu-item.p-mod-collapsed,
/* </DEPRECATED> */
.lm-Menu-item.lm-mod-hidden,
.lm-Menu-item.lm-mod-collapsed {
  display: none !important;
}


/* <DEPRECATED> */
.p-Menu-itemIcon,
.p-Menu-itemSubmenuIcon,
/* </DEPRECATED> */
.lm-Menu-itemIcon,
.lm-Menu-itemSubmenuIcon {
  display: table-cell;
  text-align: center;
}


/* <DEPRECATED> */ .p-Menu-itemLabel, /* </DEPRECATED> */
.lm-Menu-itemLabel {
  display: table-cell;
  text-align: left;
}


/* <DEPRECATED> */ .p-Menu-itemShortcut, /* </DEPRECATED> */
.lm-Menu-itemShortcut {
  display: table-cell;
  text-align: right;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-MenuBar, /* </DEPRECATED> */
.lm-MenuBar {
  outline: none;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}


/* <DEPRECATED> */ .p-MenuBar-content, /* </DEPRECATED> */
.lm-MenuBar-content {
  margin: 0;
  padding: 0;
  display: flex;
  flex-direction: row;
  list-style-type: none;
}


/* <DEPRECATED> */ .p--MenuBar-item, /* </DEPRECATED> */
.lm-MenuBar-item {
  box-sizing: border-box;
}


/* <DEPRECATED> */
.p-MenuBar-itemIcon,
.p-MenuBar-itemLabel,
/* </DEPRECATED> */
.lm-MenuBar-itemIcon,
.lm-MenuBar-itemLabel {
  display: inline-block;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-ScrollBar, /* </DEPRECATED> */
.lm-ScrollBar {
  display: flex;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}


/* <DEPRECATED> */
.p-ScrollBar[data-orientation='horizontal'],
/* </DEPRECATED> */
.lm-ScrollBar[data-orientation='horizontal'] {
  flex-direction: row;
}


/* <DEPRECATED> */
.p-ScrollBar[data-orientation='vertical'],
/* </DEPRECATED> */
.lm-ScrollBar[data-orientation='vertical'] {
  flex-direction: column;
}


/* <DEPRECATED> */ .p-ScrollBar-button, /* </DEPRECATED> */
.lm-ScrollBar-button {
  box-sizing: border-box;
  flex: 0 0 auto;
}


/* <DEPRECATED> */ .p-ScrollBar-track, /* </DEPRECATED> */
.lm-ScrollBar-track {
  box-sizing: border-box;
  position: relative;
  overflow: hidden;
  flex: 1 1 auto;
}


/* <DEPRECATED> */ .p-ScrollBar-thumb, /* </DEPRECATED> */
.lm-ScrollBar-thumb {
  box-sizing: border-box;
  position: absolute;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-SplitPanel-child, /* </DEPRECATED> */
.lm-SplitPanel-child {
  z-index: 0;
}


/* <DEPRECATED> */ .p-SplitPanel-handle, /* </DEPRECATED> */
.lm-SplitPanel-handle {
  z-index: 1;
}


/* <DEPRECATED> */ .p-SplitPanel-handle.p-mod-hidden, /* </DEPRECATED> */
.lm-SplitPanel-handle.lm-mod-hidden {
  display: none !important;
}


/* <DEPRECATED> */ .p-SplitPanel-handle:after, /* </DEPRECATED> */
.lm-SplitPanel-handle:after {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  content: '';
}


/* <DEPRECATED> */
.p-SplitPanel[data-orientation='horizontal'] > .p-SplitPanel-handle,
/* </DEPRECATED> */
.lm-SplitPanel[data-orientation='horizontal'] > .lm-SplitPanel-handle {
  cursor: ew-resize;
}


/* <DEPRECATED> */
.p-SplitPanel[data-orientation='vertical'] > .p-SplitPanel-handle,
/* </DEPRECATED> */
.lm-SplitPanel[data-orientation='vertical'] > .lm-SplitPanel-handle {
  cursor: ns-resize;
}


/* <DEPRECATED> */
.p-SplitPanel[data-orientation='horizontal'] > .p-SplitPanel-handle:after,
/* </DEPRECATED> */
.lm-SplitPanel[data-orientation='horizontal'] > .lm-SplitPanel-handle:after {
  left: 50%;
  min-width: 8px;
  transform: translateX(-50%);
}


/* <DEPRECATED> */
.p-SplitPanel[data-orientation='vertical'] > .p-SplitPanel-handle:after,
/* </DEPRECATED> */
.lm-SplitPanel[data-orientation='vertical'] > .lm-SplitPanel-handle:after {
  top: 50%;
  min-height: 8px;
  transform: translateY(-50%);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-TabBar, /* </DEPRECATED> */
.lm-TabBar {
  display: flex;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}


/* <DEPRECATED> */ .p-TabBar[data-orientation='horizontal'], /* </DEPRECATED> */
.lm-TabBar[data-orientation='horizontal'] {
  flex-direction: row;
  align-items: flex-end;
}


/* <DEPRECATED> */ .p-TabBar[data-orientation='vertical'], /* </DEPRECATED> */
.lm-TabBar[data-orientation='vertical'] {
  flex-direction: column;
  align-items: flex-end;
}


/* <DEPRECATED> */ .p-TabBar-content, /* </DEPRECATED> */
.lm-TabBar-content {
  margin: 0;
  padding: 0;
  display: flex;
  flex: 1 1 auto;
  list-style-type: none;
}


/* <DEPRECATED> */
.p-TabBar[data-orientation='horizontal'] > .p-TabBar-content,
/* </DEPRECATED> */
.lm-TabBar[data-orientation='horizontal'] > .lm-TabBar-content {
  flex-direction: row;
}


/* <DEPRECATED> */
.p-TabBar[data-orientation='vertical'] > .p-TabBar-content,
/* </DEPRECATED> */
.lm-TabBar[data-orientation='vertical'] > .lm-TabBar-content {
  flex-direction: column;
}


/* <DEPRECATED> */ .p-TabBar-tab, /* </DEPRECATED> */
.lm-TabBar-tab {
  display: flex;
  flex-direction: row;
  box-sizing: border-box;
  overflow: hidden;
}


/* <DEPRECATED> */
.p-TabBar-tabIcon,
.p-TabBar-tabCloseIcon,
/* </DEPRECATED> */
.lm-TabBar-tabIcon,
.lm-TabBar-tabCloseIcon {
  flex: 0 0 auto;
}


/* <DEPRECATED> */ .p-TabBar-tabLabel, /* </DEPRECATED> */
.lm-TabBar-tabLabel {
  flex: 1 1 auto;
  overflow: hidden;
  white-space: nowrap;
}


.lm-TabBar-tabInput {
  user-select: all;
  width: 100%;
  box-sizing : border-box;
}


/* <DEPRECATED> */ .p-TabBar-tab.p-mod-hidden, /* </DEPRECATED> */
.lm-TabBar-tab.lm-mod-hidden {
  display: none !important;
}


.lm-TabBar-addButton.lm-mod-hidden {
  display: none !important;
}


/* <DEPRECATED> */ .p-TabBar.p-mod-dragging .p-TabBar-tab, /* </DEPRECATED> */
.lm-TabBar.lm-mod-dragging .lm-TabBar-tab {
  position: relative;
}


/* <DEPRECATED> */
.p-TabBar.p-mod-dragging[data-orientation='horizontal'] .p-TabBar-tab,
/* </DEPRECATED> */
.lm-TabBar.lm-mod-dragging[data-orientation='horizontal'] .lm-TabBar-tab {
  left: 0;
  transition: left 150ms ease;
}


/* <DEPRECATED> */
.p-TabBar.p-mod-dragging[data-orientation='vertical'] .p-TabBar-tab,
/* </DEPRECATED> */
.lm-TabBar.lm-mod-dragging[data-orientation='vertical'] .lm-TabBar-tab {
  top: 0;
  transition: top 150ms ease;
}


/* <DEPRECATED> */
.p-TabBar.p-mod-dragging .p-TabBar-tab.p-mod-dragging,
/* </DEPRECATED> */
.lm-TabBar.lm-mod-dragging .lm-TabBar-tab.lm-mod-dragging {
  transition: none;
}

.lm-TabBar-tabLabel .lm-TabBar-tabInput {
  user-select: all;
  width: 100%;
  box-sizing : border-box;
  background: inherit;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-TabPanel-tabBar, /* </DEPRECATED> */
.lm-TabPanel-tabBar {
  z-index: 1;
}


/* <DEPRECATED> */ .p-TabPanel-stackedPanel, /* </DEPRECATED> */
.lm-TabPanel-stackedPanel {
  z-index: 0;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/

@charset "UTF-8";
html{
  -webkit-box-sizing:border-box;
          box-sizing:border-box; }

*,
*::before,
*::after{
  -webkit-box-sizing:inherit;
          box-sizing:inherit; }

body{
  font-size:14px;
  font-weight:400;
  letter-spacing:0;
  line-height:1.28581;
  text-transform:none;
  color:#182026;
  font-family:-apple-system, "BlinkMacSystemFont", "Segoe UI", "Roboto", "Oxygen", "Ubuntu", "Cantarell", "Open Sans", "Helvetica Neue", "Icons16", sans-serif; }

p{
  margin-bottom:10px;
  margin-top:0; }

small{
  font-size:12px; }

strong{
  font-weight:600; }

::-moz-selection{
  background:rgba(125, 188, 255, 0.6); }

::selection{
  background:rgba(125, 188, 255, 0.6); }
.bp3-heading{
  color:#182026;
  font-weight:600;
  margin:0 0 10px;
  padding:0; }
  .bp3-dark .bp3-heading{
    color:#f5f8fa; }

h1.bp3-heading, .bp3-running-text h1{
  font-size:36px;
  line-height:40px; }

h2.bp3-heading, .bp3-running-text h2{
  font-size:28px;
  line-height:32px; }

h3.bp3-heading, .bp3-running-text h3{
  font-size:22px;
  line-height:25px; }

h4.bp3-heading, .bp3-running-text h4{
  font-size:18px;
  line-height:21px; }

h5.bp3-heading, .bp3-running-text h5{
  font-size:16px;
  line-height:19px; }

h6.bp3-heading, .bp3-running-text h6{
  font-size:14px;
  line-height:16px; }
.bp3-ui-text{
  font-size:14px;
  font-weight:400;
  letter-spacing:0;
  line-height:1.28581;
  text-transform:none; }

.bp3-monospace-text{
  font-family:monospace;
  text-transform:none; }

.bp3-text-muted{
  color:#5c7080; }
  .bp3-dark .bp3-text-muted{
    color:#a7b6c2; }

.bp3-text-disabled{
  color:rgba(92, 112, 128, 0.6); }
  .bp3-dark .bp3-text-disabled{
    color:rgba(167, 182, 194, 0.6); }

.bp3-text-overflow-ellipsis{
  overflow:hidden;
  text-overflow:ellipsis;
  white-space:nowrap;
  word-wrap:normal; }
.bp3-running-text{
  font-size:14px;
  line-height:1.5; }
  .bp3-running-text h1{
    color:#182026;
    font-weight:600;
    margin-bottom:20px;
    margin-top:40px; }
    .bp3-dark .bp3-running-text h1{
      color:#f5f8fa; }
  .bp3-running-text h2{
    color:#182026;
    font-weight:600;
    margin-bottom:20px;
    margin-top:40px; }
    .bp3-dark .bp3-running-text h2{
      color:#f5f8fa; }
  .bp3-running-text h3{
    color:#182026;
    font-weight:600;
    margin-bottom:20px;
    margin-top:40px; }
    .bp3-dark .bp3-running-text h3{
      color:#f5f8fa; }
  .bp3-running-text h4{
    color:#182026;
    font-weight:600;
    margin-bottom:20px;
    margin-top:40px; }
    .bp3-dark .bp3-running-text h4{
      color:#f5f8fa; }
  .bp3-running-text h5{
    color:#182026;
    font-weight:600;
    margin-bottom:20px;
    margin-top:40px; }
    .bp3-dark .bp3-running-text h5{
      color:#f5f8fa; }
  .bp3-running-text h6{
    color:#182026;
    font-weight:600;
    margin-bottom:20px;
    margin-top:40px; }
    .bp3-dark .bp3-running-text h6{
      color:#f5f8fa; }
  .bp3-running-text hr{
    border:none;
    border-bottom:1px solid rgba(16, 22, 26, 0.15);
    margin:20px 0; }
    .bp3-dark .bp3-running-text hr{
      border-color:rgba(255, 255, 255, 0.15); }
  .bp3-running-text p{
    margin:0 0 10px;
    padding:0; }

.bp3-text-large{
  font-size:16px; }

.bp3-text-small{
  font-size:12px; }
a{
  color:#106ba3;
  text-decoration:none; }
  a:hover{
    color:#106ba3;
    cursor:pointer;
    text-decoration:underline; }
  a .bp3-icon, a .bp3-icon-standard, a .bp3-icon-large{
    color:inherit; }
  a code,
  .bp3-dark a code{
    color:inherit; }
  .bp3-dark a,
  .bp3-dark a:hover{
    color:#48aff0; }
    .bp3-dark a .bp3-icon, .bp3-dark a .bp3-icon-standard, .bp3-dark a .bp3-icon-large,
    .bp3-dark a:hover .bp3-icon,
    .bp3-dark a:hover .bp3-icon-standard,
    .bp3-dark a:hover .bp3-icon-large{
      color:inherit; }
.bp3-running-text code, .bp3-code{
  font-family:monospace;
  text-transform:none;
  background:rgba(255, 255, 255, 0.7);
  border-radius:3px;
  -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2);
          box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2);
  color:#5c7080;
  font-size:smaller;
  padding:2px 5px; }
  .bp3-dark .bp3-running-text code, .bp3-running-text .bp3-dark code, .bp3-dark .bp3-code{
    background:rgba(16, 22, 26, 0.3);
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
    color:#a7b6c2; }
  .bp3-running-text a > code, a > .bp3-code{
    color:#137cbd; }
    .bp3-dark .bp3-running-text a > code, .bp3-running-text .bp3-dark a > code, .bp3-dark a > .bp3-code{
      color:inherit; }

.bp3-running-text pre, .bp3-code-block{
  font-family:monospace;
  text-transform:none;
  background:rgba(255, 255, 255, 0.7);
  border-radius:3px;
  -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.15);
          box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.15);
  color:#182026;
  display:block;
  font-size:13px;
  line-height:1.4;
  margin:10px 0;
  padding:13px 15px 12px;
  word-break:break-all;
  word-wrap:break-word; }
  .bp3-dark .bp3-running-text pre, .bp3-running-text .bp3-dark pre, .bp3-dark .bp3-code-block{
    background:rgba(16, 22, 26, 0.3);
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
    color:#f5f8fa; }
  .bp3-running-text pre > code, .bp3-code-block > code{
    background:none;
    -webkit-box-shadow:none;
            box-shadow:none;
    color:inherit;
    font-size:inherit;
    padding:0; }

.bp3-running-text kbd, .bp3-key{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  background:#ffffff;
  border-radius:3px;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2);
  color:#5c7080;
  display:-webkit-inline-box;
  display:-ms-inline-flexbox;
  display:inline-flex;
  font-family:inherit;
  font-size:12px;
  height:24px;
  -webkit-box-pack:center;
      -ms-flex-pack:center;
          justify-content:center;
  line-height:24px;
  min-width:24px;
  padding:3px 6px;
  vertical-align:middle; }
  .bp3-running-text kbd .bp3-icon, .bp3-key .bp3-icon, .bp3-running-text kbd .bp3-icon-standard, .bp3-key .bp3-icon-standard, .bp3-running-text kbd .bp3-icon-large, .bp3-key .bp3-icon-large{
    margin-right:5px; }
  .bp3-dark .bp3-running-text kbd, .bp3-running-text .bp3-dark kbd, .bp3-dark .bp3-key{
    background:#394b59;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4);
    color:#a7b6c2; }
.bp3-running-text blockquote, .bp3-blockquote{
  border-left:solid 4px rgba(167, 182, 194, 0.5);
  margin:0 0 10px;
  padding:0 20px; }
  .bp3-dark .bp3-running-text blockquote, .bp3-running-text .bp3-dark blockquote, .bp3-dark .bp3-blockquote{
    border-color:rgba(115, 134, 148, 0.5); }
.bp3-running-text ul,
.bp3-running-text ol, .bp3-list{
  margin:10px 0;
  padding-left:30px; }
  .bp3-running-text ul li:not(:last-child), .bp3-running-text ol li:not(:last-child), .bp3-list li:not(:last-child){
    margin-bottom:5px; }
  .bp3-running-text ul ol, .bp3-running-text ol ol, .bp3-list ol,
  .bp3-running-text ul ul,
  .bp3-running-text ol ul,
  .bp3-list ul{
    margin-top:5px; }

.bp3-list-unstyled{
  list-style:none;
  margin:0;
  padding:0; }
  .bp3-list-unstyled li{
    padding:0; }
.bp3-rtl{
  text-align:right; }

.bp3-dark{
  color:#f5f8fa; }

:focus{
  outline:rgba(19, 124, 189, 0.6) auto 2px;
  outline-offset:2px;
  -moz-outline-radius:6px; }

.bp3-focus-disabled :focus{
  outline:none !important; }
  .bp3-focus-disabled :focus ~ .bp3-control-indicator{
    outline:none !important; }

.bp3-alert{
  max-width:400px;
  padding:20px; }

.bp3-alert-body{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex; }
  .bp3-alert-body .bp3-icon{
    font-size:40px;
    margin-right:20px;
    margin-top:0; }

.bp3-alert-contents{
  word-break:break-word; }

.bp3-alert-footer{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:reverse;
      -ms-flex-direction:row-reverse;
          flex-direction:row-reverse;
  margin-top:10px; }
  .bp3-alert-footer .bp3-button{
    margin-left:10px; }
.bp3-breadcrumbs{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  cursor:default;
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -ms-flex-wrap:wrap;
      flex-wrap:wrap;
  height:30px;
  list-style:none;
  margin:0;
  padding:0; }
  .bp3-breadcrumbs > li{
    -webkit-box-align:center;
        -ms-flex-align:center;
            align-items:center;
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex; }
    .bp3-breadcrumbs > li::after{
      background:url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 16 16'%3e%3cpath fill-rule='evenodd' clip-rule='evenodd' d='M10.71 7.29l-4-4a1.003 1.003 0 00-1.42 1.42L8.59 8 5.3 11.29c-.19.18-.3.43-.3.71a1.003 1.003 0 001.71.71l4-4c.18-.18.29-.43.29-.71 0-.28-.11-.53-.29-.71z' fill='%235C7080'/%3e%3c/svg%3e");
      content:"";
      display:block;
      height:16px;
      margin:0 5px;
      width:16px; }
    .bp3-breadcrumbs > li:last-of-type::after{
      display:none; }

.bp3-breadcrumb,
.bp3-breadcrumb-current,
.bp3-breadcrumbs-collapsed{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  display:-webkit-inline-box;
  display:-ms-inline-flexbox;
  display:inline-flex;
  font-size:16px; }

.bp3-breadcrumb,
.bp3-breadcrumbs-collapsed{
  color:#5c7080; }

.bp3-breadcrumb:hover{
  text-decoration:none; }

.bp3-breadcrumb.bp3-disabled{
  color:rgba(92, 112, 128, 0.6);
  cursor:not-allowed; }

.bp3-breadcrumb .bp3-icon{
  margin-right:5px; }

.bp3-breadcrumb-current{
  color:inherit;
  font-weight:600; }
  .bp3-breadcrumb-current .bp3-input{
    font-size:inherit;
    font-weight:inherit;
    vertical-align:baseline; }

.bp3-breadcrumbs-collapsed{
  background:#ced9e0;
  border:none;
  border-radius:3px;
  cursor:pointer;
  margin-right:2px;
  padding:1px 5px;
  vertical-align:text-bottom; }
  .bp3-breadcrumbs-collapsed::before{
    background:url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 16 16'%3e%3cg fill='%235C7080'%3e%3ccircle cx='2' cy='8.03' r='2'/%3e%3ccircle cx='14' cy='8.03' r='2'/%3e%3ccircle cx='8' cy='8.03' r='2'/%3e%3c/g%3e%3c/svg%3e") center no-repeat;
    content:"";
    display:block;
    height:16px;
    width:16px; }
  .bp3-breadcrumbs-collapsed:hover{
    background:#bfccd6;
    color:#182026;
    text-decoration:none; }

.bp3-dark .bp3-breadcrumb,
.bp3-dark .bp3-breadcrumbs-collapsed{
  color:#a7b6c2; }

.bp3-dark .bp3-breadcrumbs > li::after{
  color:#a7b6c2; }

.bp3-dark .bp3-breadcrumb.bp3-disabled{
  color:rgba(167, 182, 194, 0.6); }

.bp3-dark .bp3-breadcrumb-current{
  color:#f5f8fa; }

.bp3-dark .bp3-breadcrumbs-collapsed{
  background:rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-breadcrumbs-collapsed:hover{
    background:rgba(16, 22, 26, 0.6);
    color:#f5f8fa; }
.bp3-button{
  display:-webkit-inline-box;
  display:-ms-inline-flexbox;
  display:inline-flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:normal;
      -ms-flex-direction:row;
          flex-direction:row;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  border:none;
  border-radius:3px;
  cursor:pointer;
  font-size:14px;
  -webkit-box-pack:center;
      -ms-flex-pack:center;
          justify-content:center;
  padding:5px 10px;
  text-align:left;
  vertical-align:middle;
  min-height:30px;
  min-width:30px; }
  .bp3-button > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-button > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-button::before,
  .bp3-button > *{
    margin-right:7px; }
  .bp3-button:empty::before,
  .bp3-button > :last-child{
    margin-right:0; }
  .bp3-button:empty{
    padding:0 !important; }
  .bp3-button:disabled, .bp3-button.bp3-disabled{
    cursor:not-allowed; }
  .bp3-button.bp3-fill{
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    width:100%; }
  .bp3-button.bp3-align-right,
  .bp3-align-right .bp3-button{
    text-align:right; }
  .bp3-button.bp3-align-left,
  .bp3-align-left .bp3-button{
    text-align:left; }
  .bp3-button:not([class*="bp3-intent-"]){
    background-color:#f5f8fa;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.8)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.8), rgba(255, 255, 255, 0));
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
    color:#182026; }
    .bp3-button:not([class*="bp3-intent-"]):hover{
      background-clip:padding-box;
      background-color:#ebf1f5;
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1); }
    .bp3-button:not([class*="bp3-intent-"]):active, .bp3-button:not([class*="bp3-intent-"]).bp3-active{
      background-color:#d8e1e8;
      background-image:none;
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
    .bp3-button:not([class*="bp3-intent-"]):disabled, .bp3-button:not([class*="bp3-intent-"]).bp3-disabled{
      background-color:rgba(206, 217, 224, 0.5);
      background-image:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(92, 112, 128, 0.6);
      cursor:not-allowed;
      outline:none; }
      .bp3-button:not([class*="bp3-intent-"]):disabled.bp3-active, .bp3-button:not([class*="bp3-intent-"]):disabled.bp3-active:hover, .bp3-button:not([class*="bp3-intent-"]).bp3-disabled.bp3-active, .bp3-button:not([class*="bp3-intent-"]).bp3-disabled.bp3-active:hover{
        background:rgba(206, 217, 224, 0.7); }
  .bp3-button.bp3-intent-primary{
    background-color:#137cbd;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.1)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.1), rgba(255, 255, 255, 0));
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
    color:#ffffff; }
    .bp3-button.bp3-intent-primary:hover, .bp3-button.bp3-intent-primary:active, .bp3-button.bp3-intent-primary.bp3-active{
      color:#ffffff; }
    .bp3-button.bp3-intent-primary:hover{
      background-color:#106ba3;
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2); }
    .bp3-button.bp3-intent-primary:active, .bp3-button.bp3-intent-primary.bp3-active{
      background-color:#0e5a8a;
      background-image:none;
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
    .bp3-button.bp3-intent-primary:disabled, .bp3-button.bp3-intent-primary.bp3-disabled{
      background-color:rgba(19, 124, 189, 0.5);
      background-image:none;
      border-color:transparent;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(255, 255, 255, 0.6); }
  .bp3-button.bp3-intent-success{
    background-color:#0f9960;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.1)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.1), rgba(255, 255, 255, 0));
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
    color:#ffffff; }
    .bp3-button.bp3-intent-success:hover, .bp3-button.bp3-intent-success:active, .bp3-button.bp3-intent-success.bp3-active{
      color:#ffffff; }
    .bp3-button.bp3-intent-success:hover{
      background-color:#0d8050;
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2); }
    .bp3-button.bp3-intent-success:active, .bp3-button.bp3-intent-success.bp3-active{
      background-color:#0a6640;
      background-image:none;
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
    .bp3-button.bp3-intent-success:disabled, .bp3-button.bp3-intent-success.bp3-disabled{
      background-color:rgba(15, 153, 96, 0.5);
      background-image:none;
      border-color:transparent;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(255, 255, 255, 0.6); }
  .bp3-button.bp3-intent-warning{
    background-color:#d9822b;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.1)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.1), rgba(255, 255, 255, 0));
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
    color:#ffffff; }
    .bp3-button.bp3-intent-warning:hover, .bp3-button.bp3-intent-warning:active, .bp3-button.bp3-intent-warning.bp3-active{
      color:#ffffff; }
    .bp3-button.bp3-intent-warning:hover{
      background-color:#bf7326;
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2); }
    .bp3-button.bp3-intent-warning:active, .bp3-button.bp3-intent-warning.bp3-active{
      background-color:#a66321;
      background-image:none;
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
    .bp3-button.bp3-intent-warning:disabled, .bp3-button.bp3-intent-warning.bp3-disabled{
      background-color:rgba(217, 130, 43, 0.5);
      background-image:none;
      border-color:transparent;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(255, 255, 255, 0.6); }
  .bp3-button.bp3-intent-danger{
    background-color:#db3737;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.1)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.1), rgba(255, 255, 255, 0));
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
    color:#ffffff; }
    .bp3-button.bp3-intent-danger:hover, .bp3-button.bp3-intent-danger:active, .bp3-button.bp3-intent-danger.bp3-active{
      color:#ffffff; }
    .bp3-button.bp3-intent-danger:hover{
      background-color:#c23030;
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2); }
    .bp3-button.bp3-intent-danger:active, .bp3-button.bp3-intent-danger.bp3-active{
      background-color:#a82a2a;
      background-image:none;
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
    .bp3-button.bp3-intent-danger:disabled, .bp3-button.bp3-intent-danger.bp3-disabled{
      background-color:rgba(219, 55, 55, 0.5);
      background-image:none;
      border-color:transparent;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(255, 255, 255, 0.6); }
  .bp3-button[class*="bp3-intent-"] .bp3-button-spinner .bp3-spinner-head{
    stroke:#ffffff; }
  .bp3-button.bp3-large,
  .bp3-large .bp3-button{
    min-height:40px;
    min-width:40px;
    font-size:16px;
    padding:5px 15px; }
    .bp3-button.bp3-large::before,
    .bp3-button.bp3-large > *,
    .bp3-large .bp3-button::before,
    .bp3-large .bp3-button > *{
      margin-right:10px; }
    .bp3-button.bp3-large:empty::before,
    .bp3-button.bp3-large > :last-child,
    .bp3-large .bp3-button:empty::before,
    .bp3-large .bp3-button > :last-child{
      margin-right:0; }
  .bp3-button.bp3-small,
  .bp3-small .bp3-button{
    min-height:24px;
    min-width:24px;
    padding:0 7px; }
  .bp3-button.bp3-loading{
    position:relative; }
    .bp3-button.bp3-loading[class*="bp3-icon-"]::before{
      visibility:hidden; }
    .bp3-button.bp3-loading .bp3-button-spinner{
      margin:0;
      position:absolute; }
    .bp3-button.bp3-loading > :not(.bp3-button-spinner){
      visibility:hidden; }
  .bp3-button[class*="bp3-icon-"]::before{
    font-family:"Icons16", sans-serif;
    font-size:16px;
    font-style:normal;
    font-weight:400;
    line-height:1;
    -moz-osx-font-smoothing:grayscale;
    -webkit-font-smoothing:antialiased;
    color:#5c7080; }
  .bp3-button .bp3-icon, .bp3-button .bp3-icon-standard, .bp3-button .bp3-icon-large{
    color:#5c7080; }
    .bp3-button .bp3-icon.bp3-align-right, .bp3-button .bp3-icon-standard.bp3-align-right, .bp3-button .bp3-icon-large.bp3-align-right{
      margin-left:7px; }
  .bp3-button .bp3-icon:first-child:last-child,
  .bp3-button .bp3-spinner + .bp3-icon:last-child{
    margin:0 -7px; }
  .bp3-dark .bp3-button:not([class*="bp3-intent-"]){
    background-color:#394b59;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.05)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.05), rgba(255, 255, 255, 0));
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
    color:#f5f8fa; }
    .bp3-dark .bp3-button:not([class*="bp3-intent-"]):hover, .bp3-dark .bp3-button:not([class*="bp3-intent-"]):active, .bp3-dark .bp3-button:not([class*="bp3-intent-"]).bp3-active{
      color:#f5f8fa; }
    .bp3-dark .bp3-button:not([class*="bp3-intent-"]):hover{
      background-color:#30404d;
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-button:not([class*="bp3-intent-"]):active, .bp3-dark .bp3-button:not([class*="bp3-intent-"]).bp3-active{
      background-color:#202b33;
      background-image:none;
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
    .bp3-dark .bp3-button:not([class*="bp3-intent-"]):disabled, .bp3-dark .bp3-button:not([class*="bp3-intent-"]).bp3-disabled{
      background-color:rgba(57, 75, 89, 0.5);
      background-image:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(167, 182, 194, 0.6); }
      .bp3-dark .bp3-button:not([class*="bp3-intent-"]):disabled.bp3-active, .bp3-dark .bp3-button:not([class*="bp3-intent-"]).bp3-disabled.bp3-active{
        background:rgba(57, 75, 89, 0.7); }
    .bp3-dark .bp3-button:not([class*="bp3-intent-"]) .bp3-button-spinner .bp3-spinner-head{
      background:rgba(16, 22, 26, 0.5);
      stroke:#8a9ba8; }
    .bp3-dark .bp3-button:not([class*="bp3-intent-"])[class*="bp3-icon-"]::before{
      color:#a7b6c2; }
    .bp3-dark .bp3-button:not([class*="bp3-intent-"]) .bp3-icon, .bp3-dark .bp3-button:not([class*="bp3-intent-"]) .bp3-icon-standard, .bp3-dark .bp3-button:not([class*="bp3-intent-"]) .bp3-icon-large{
      color:#a7b6c2; }
  .bp3-dark .bp3-button[class*="bp3-intent-"]{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-button[class*="bp3-intent-"]:hover{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-button[class*="bp3-intent-"]:active, .bp3-dark .bp3-button[class*="bp3-intent-"].bp3-active{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
    .bp3-dark .bp3-button[class*="bp3-intent-"]:disabled, .bp3-dark .bp3-button[class*="bp3-intent-"].bp3-disabled{
      background-image:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(255, 255, 255, 0.3); }
    .bp3-dark .bp3-button[class*="bp3-intent-"] .bp3-button-spinner .bp3-spinner-head{
      stroke:#8a9ba8; }
  .bp3-button:disabled::before,
  .bp3-button:disabled .bp3-icon, .bp3-button:disabled .bp3-icon-standard, .bp3-button:disabled .bp3-icon-large, .bp3-button.bp3-disabled::before,
  .bp3-button.bp3-disabled .bp3-icon, .bp3-button.bp3-disabled .bp3-icon-standard, .bp3-button.bp3-disabled .bp3-icon-large, .bp3-button[class*="bp3-intent-"]::before,
  .bp3-button[class*="bp3-intent-"] .bp3-icon, .bp3-button[class*="bp3-intent-"] .bp3-icon-standard, .bp3-button[class*="bp3-intent-"] .bp3-icon-large{
    color:inherit !important; }
  .bp3-button.bp3-minimal{
    background:none;
    -webkit-box-shadow:none;
            box-shadow:none; }
    .bp3-button.bp3-minimal:hover{
      background:rgba(167, 182, 194, 0.3);
      -webkit-box-shadow:none;
              box-shadow:none;
      color:#182026;
      text-decoration:none; }
    .bp3-button.bp3-minimal:active, .bp3-button.bp3-minimal.bp3-active{
      background:rgba(115, 134, 148, 0.3);
      -webkit-box-shadow:none;
              box-shadow:none;
      color:#182026; }
    .bp3-button.bp3-minimal:disabled, .bp3-button.bp3-minimal:disabled:hover, .bp3-button.bp3-minimal.bp3-disabled, .bp3-button.bp3-minimal.bp3-disabled:hover{
      background:none;
      color:rgba(92, 112, 128, 0.6);
      cursor:not-allowed; }
      .bp3-button.bp3-minimal:disabled.bp3-active, .bp3-button.bp3-minimal:disabled:hover.bp3-active, .bp3-button.bp3-minimal.bp3-disabled.bp3-active, .bp3-button.bp3-minimal.bp3-disabled:hover.bp3-active{
        background:rgba(115, 134, 148, 0.3); }
    .bp3-dark .bp3-button.bp3-minimal{
      background:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:inherit; }
      .bp3-dark .bp3-button.bp3-minimal:hover, .bp3-dark .bp3-button.bp3-minimal:active, .bp3-dark .bp3-button.bp3-minimal.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none; }
      .bp3-dark .bp3-button.bp3-minimal:hover{
        background:rgba(138, 155, 168, 0.15); }
      .bp3-dark .bp3-button.bp3-minimal:active, .bp3-dark .bp3-button.bp3-minimal.bp3-active{
        background:rgba(138, 155, 168, 0.3);
        color:#f5f8fa; }
      .bp3-dark .bp3-button.bp3-minimal:disabled, .bp3-dark .bp3-button.bp3-minimal:disabled:hover, .bp3-dark .bp3-button.bp3-minimal.bp3-disabled, .bp3-dark .bp3-button.bp3-minimal.bp3-disabled:hover{
        background:none;
        color:rgba(167, 182, 194, 0.6);
        cursor:not-allowed; }
        .bp3-dark .bp3-button.bp3-minimal:disabled.bp3-active, .bp3-dark .bp3-button.bp3-minimal:disabled:hover.bp3-active, .bp3-dark .bp3-button.bp3-minimal.bp3-disabled.bp3-active, .bp3-dark .bp3-button.bp3-minimal.bp3-disabled:hover.bp3-active{
          background:rgba(138, 155, 168, 0.3); }
    .bp3-button.bp3-minimal.bp3-intent-primary{
      color:#106ba3; }
      .bp3-button.bp3-minimal.bp3-intent-primary:hover, .bp3-button.bp3-minimal.bp3-intent-primary:active, .bp3-button.bp3-minimal.bp3-intent-primary.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:#106ba3; }
      .bp3-button.bp3-minimal.bp3-intent-primary:hover{
        background:rgba(19, 124, 189, 0.15);
        color:#106ba3; }
      .bp3-button.bp3-minimal.bp3-intent-primary:active, .bp3-button.bp3-minimal.bp3-intent-primary.bp3-active{
        background:rgba(19, 124, 189, 0.3);
        color:#106ba3; }
      .bp3-button.bp3-minimal.bp3-intent-primary:disabled, .bp3-button.bp3-minimal.bp3-intent-primary.bp3-disabled{
        background:none;
        color:rgba(16, 107, 163, 0.5); }
        .bp3-button.bp3-minimal.bp3-intent-primary:disabled.bp3-active, .bp3-button.bp3-minimal.bp3-intent-primary.bp3-disabled.bp3-active{
          background:rgba(19, 124, 189, 0.3); }
      .bp3-button.bp3-minimal.bp3-intent-primary .bp3-button-spinner .bp3-spinner-head{
        stroke:#106ba3; }
      .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary{
        color:#48aff0; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary:hover{
          background:rgba(19, 124, 189, 0.2);
          color:#48aff0; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary:active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary.bp3-active{
          background:rgba(19, 124, 189, 0.3);
          color:#48aff0; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary:disabled, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary.bp3-disabled{
          background:none;
          color:rgba(72, 175, 240, 0.5); }
          .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary:disabled.bp3-active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary.bp3-disabled.bp3-active{
            background:rgba(19, 124, 189, 0.3); }
    .bp3-button.bp3-minimal.bp3-intent-success{
      color:#0d8050; }
      .bp3-button.bp3-minimal.bp3-intent-success:hover, .bp3-button.bp3-minimal.bp3-intent-success:active, .bp3-button.bp3-minimal.bp3-intent-success.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:#0d8050; }
      .bp3-button.bp3-minimal.bp3-intent-success:hover{
        background:rgba(15, 153, 96, 0.15);
        color:#0d8050; }
      .bp3-button.bp3-minimal.bp3-intent-success:active, .bp3-button.bp3-minimal.bp3-intent-success.bp3-active{
        background:rgba(15, 153, 96, 0.3);
        color:#0d8050; }
      .bp3-button.bp3-minimal.bp3-intent-success:disabled, .bp3-button.bp3-minimal.bp3-intent-success.bp3-disabled{
        background:none;
        color:rgba(13, 128, 80, 0.5); }
        .bp3-button.bp3-minimal.bp3-intent-success:disabled.bp3-active, .bp3-button.bp3-minimal.bp3-intent-success.bp3-disabled.bp3-active{
          background:rgba(15, 153, 96, 0.3); }
      .bp3-button.bp3-minimal.bp3-intent-success .bp3-button-spinner .bp3-spinner-head{
        stroke:#0d8050; }
      .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success{
        color:#3dcc91; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success:hover{
          background:rgba(15, 153, 96, 0.2);
          color:#3dcc91; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success:active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success.bp3-active{
          background:rgba(15, 153, 96, 0.3);
          color:#3dcc91; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success:disabled, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success.bp3-disabled{
          background:none;
          color:rgba(61, 204, 145, 0.5); }
          .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success:disabled.bp3-active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success.bp3-disabled.bp3-active{
            background:rgba(15, 153, 96, 0.3); }
    .bp3-button.bp3-minimal.bp3-intent-warning{
      color:#bf7326; }
      .bp3-button.bp3-minimal.bp3-intent-warning:hover, .bp3-button.bp3-minimal.bp3-intent-warning:active, .bp3-button.bp3-minimal.bp3-intent-warning.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:#bf7326; }
      .bp3-button.bp3-minimal.bp3-intent-warning:hover{
        background:rgba(217, 130, 43, 0.15);
        color:#bf7326; }
      .bp3-button.bp3-minimal.bp3-intent-warning:active, .bp3-button.bp3-minimal.bp3-intent-warning.bp3-active{
        background:rgba(217, 130, 43, 0.3);
        color:#bf7326; }
      .bp3-button.bp3-minimal.bp3-intent-warning:disabled, .bp3-button.bp3-minimal.bp3-intent-warning.bp3-disabled{
        background:none;
        color:rgba(191, 115, 38, 0.5); }
        .bp3-button.bp3-minimal.bp3-intent-warning:disabled.bp3-active, .bp3-button.bp3-minimal.bp3-intent-warning.bp3-disabled.bp3-active{
          background:rgba(217, 130, 43, 0.3); }
      .bp3-button.bp3-minimal.bp3-intent-warning .bp3-button-spinner .bp3-spinner-head{
        stroke:#bf7326; }
      .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning{
        color:#ffb366; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning:hover{
          background:rgba(217, 130, 43, 0.2);
          color:#ffb366; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning:active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning.bp3-active{
          background:rgba(217, 130, 43, 0.3);
          color:#ffb366; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning:disabled, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning.bp3-disabled{
          background:none;
          color:rgba(255, 179, 102, 0.5); }
          .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning:disabled.bp3-active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning.bp3-disabled.bp3-active{
            background:rgba(217, 130, 43, 0.3); }
    .bp3-button.bp3-minimal.bp3-intent-danger{
      color:#c23030; }
      .bp3-button.bp3-minimal.bp3-intent-danger:hover, .bp3-button.bp3-minimal.bp3-intent-danger:active, .bp3-button.bp3-minimal.bp3-intent-danger.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:#c23030; }
      .bp3-button.bp3-minimal.bp3-intent-danger:hover{
        background:rgba(219, 55, 55, 0.15);
        color:#c23030; }
      .bp3-button.bp3-minimal.bp3-intent-danger:active, .bp3-button.bp3-minimal.bp3-intent-danger.bp3-active{
        background:rgba(219, 55, 55, 0.3);
        color:#c23030; }
      .bp3-button.bp3-minimal.bp3-intent-danger:disabled, .bp3-button.bp3-minimal.bp3-intent-danger.bp3-disabled{
        background:none;
        color:rgba(194, 48, 48, 0.5); }
        .bp3-button.bp3-minimal.bp3-intent-danger:disabled.bp3-active, .bp3-button.bp3-minimal.bp3-intent-danger.bp3-disabled.bp3-active{
          background:rgba(219, 55, 55, 0.3); }
      .bp3-button.bp3-minimal.bp3-intent-danger .bp3-button-spinner .bp3-spinner-head{
        stroke:#c23030; }
      .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger{
        color:#ff7373; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger:hover{
          background:rgba(219, 55, 55, 0.2);
          color:#ff7373; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger:active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger.bp3-active{
          background:rgba(219, 55, 55, 0.3);
          color:#ff7373; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger:disabled, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger.bp3-disabled{
          background:none;
          color:rgba(255, 115, 115, 0.5); }
          .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger:disabled.bp3-active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger.bp3-disabled.bp3-active{
            background:rgba(219, 55, 55, 0.3); }
  .bp3-button.bp3-outlined{
    background:none;
    -webkit-box-shadow:none;
            box-shadow:none;
    border:1px solid rgba(24, 32, 38, 0.2);
    -webkit-box-sizing:border-box;
            box-sizing:border-box; }
    .bp3-button.bp3-outlined:hover{
      background:rgba(167, 182, 194, 0.3);
      -webkit-box-shadow:none;
              box-shadow:none;
      color:#182026;
      text-decoration:none; }
    .bp3-button.bp3-outlined:active, .bp3-button.bp3-outlined.bp3-active{
      background:rgba(115, 134, 148, 0.3);
      -webkit-box-shadow:none;
              box-shadow:none;
      color:#182026; }
    .bp3-button.bp3-outlined:disabled, .bp3-button.bp3-outlined:disabled:hover, .bp3-button.bp3-outlined.bp3-disabled, .bp3-button.bp3-outlined.bp3-disabled:hover{
      background:none;
      color:rgba(92, 112, 128, 0.6);
      cursor:not-allowed; }
      .bp3-button.bp3-outlined:disabled.bp3-active, .bp3-button.bp3-outlined:disabled:hover.bp3-active, .bp3-button.bp3-outlined.bp3-disabled.bp3-active, .bp3-button.bp3-outlined.bp3-disabled:hover.bp3-active{
        background:rgba(115, 134, 148, 0.3); }
    .bp3-dark .bp3-button.bp3-outlined{
      background:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:inherit; }
      .bp3-dark .bp3-button.bp3-outlined:hover, .bp3-dark .bp3-button.bp3-outlined:active, .bp3-dark .bp3-button.bp3-outlined.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none; }
      .bp3-dark .bp3-button.bp3-outlined:hover{
        background:rgba(138, 155, 168, 0.15); }
      .bp3-dark .bp3-button.bp3-outlined:active, .bp3-dark .bp3-button.bp3-outlined.bp3-active{
        background:rgba(138, 155, 168, 0.3);
        color:#f5f8fa; }
      .bp3-dark .bp3-button.bp3-outlined:disabled, .bp3-dark .bp3-button.bp3-outlined:disabled:hover, .bp3-dark .bp3-button.bp3-outlined.bp3-disabled, .bp3-dark .bp3-button.bp3-outlined.bp3-disabled:hover{
        background:none;
        color:rgba(167, 182, 194, 0.6);
        cursor:not-allowed; }
        .bp3-dark .bp3-button.bp3-outlined:disabled.bp3-active, .bp3-dark .bp3-button.bp3-outlined:disabled:hover.bp3-active, .bp3-dark .bp3-button.bp3-outlined.bp3-disabled.bp3-active, .bp3-dark .bp3-button.bp3-outlined.bp3-disabled:hover.bp3-active{
          background:rgba(138, 155, 168, 0.3); }
    .bp3-button.bp3-outlined.bp3-intent-primary{
      color:#106ba3; }
      .bp3-button.bp3-outlined.bp3-intent-primary:hover, .bp3-button.bp3-outlined.bp3-intent-primary:active, .bp3-button.bp3-outlined.bp3-intent-primary.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:#106ba3; }
      .bp3-button.bp3-outlined.bp3-intent-primary:hover{
        background:rgba(19, 124, 189, 0.15);
        color:#106ba3; }
      .bp3-button.bp3-outlined.bp3-intent-primary:active, .bp3-button.bp3-outlined.bp3-intent-primary.bp3-active{
        background:rgba(19, 124, 189, 0.3);
        color:#106ba3; }
      .bp3-button.bp3-outlined.bp3-intent-primary:disabled, .bp3-button.bp3-outlined.bp3-intent-primary.bp3-disabled{
        background:none;
        color:rgba(16, 107, 163, 0.5); }
        .bp3-button.bp3-outlined.bp3-intent-primary:disabled.bp3-active, .bp3-button.bp3-outlined.bp3-intent-primary.bp3-disabled.bp3-active{
          background:rgba(19, 124, 189, 0.3); }
      .bp3-button.bp3-outlined.bp3-intent-primary .bp3-button-spinner .bp3-spinner-head{
        stroke:#106ba3; }
      .bp3-dark .bp3-button.bp3-outlined.bp3-intent-primary{
        color:#48aff0; }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-primary:hover{
          background:rgba(19, 124, 189, 0.2);
          color:#48aff0; }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-primary:active, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-primary.bp3-active{
          background:rgba(19, 124, 189, 0.3);
          color:#48aff0; }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-primary:disabled, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-primary.bp3-disabled{
          background:none;
          color:rgba(72, 175, 240, 0.5); }
          .bp3-dark .bp3-button.bp3-outlined.bp3-intent-primary:disabled.bp3-active, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-primary.bp3-disabled.bp3-active{
            background:rgba(19, 124, 189, 0.3); }
    .bp3-button.bp3-outlined.bp3-intent-success{
      color:#0d8050; }
      .bp3-button.bp3-outlined.bp3-intent-success:hover, .bp3-button.bp3-outlined.bp3-intent-success:active, .bp3-button.bp3-outlined.bp3-intent-success.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:#0d8050; }
      .bp3-button.bp3-outlined.bp3-intent-success:hover{
        background:rgba(15, 153, 96, 0.15);
        color:#0d8050; }
      .bp3-button.bp3-outlined.bp3-intent-success:active, .bp3-button.bp3-outlined.bp3-intent-success.bp3-active{
        background:rgba(15, 153, 96, 0.3);
        color:#0d8050; }
      .bp3-button.bp3-outlined.bp3-intent-success:disabled, .bp3-button.bp3-outlined.bp3-intent-success.bp3-disabled{
        background:none;
        color:rgba(13, 128, 80, 0.5); }
        .bp3-button.bp3-outlined.bp3-intent-success:disabled.bp3-active, .bp3-button.bp3-outlined.bp3-intent-success.bp3-disabled.bp3-active{
          background:rgba(15, 153, 96, 0.3); }
      .bp3-button.bp3-outlined.bp3-intent-success .bp3-button-spinner .bp3-spinner-head{
        stroke:#0d8050; }
      .bp3-dark .bp3-button.bp3-outlined.bp3-intent-success{
        color:#3dcc91; }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-success:hover{
          background:rgba(15, 153, 96, 0.2);
          color:#3dcc91; }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-success:active, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-success.bp3-active{
          background:rgba(15, 153, 96, 0.3);
          color:#3dcc91; }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-success:disabled, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-success.bp3-disabled{
          background:none;
          color:rgba(61, 204, 145, 0.5); }
          .bp3-dark .bp3-button.bp3-outlined.bp3-intent-success:disabled.bp3-active, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-success.bp3-disabled.bp3-active{
            background:rgba(15, 153, 96, 0.3); }
    .bp3-button.bp3-outlined.bp3-intent-warning{
      color:#bf7326; }
      .bp3-button.bp3-outlined.bp3-intent-warning:hover, .bp3-button.bp3-outlined.bp3-intent-warning:active, .bp3-button.bp3-outlined.bp3-intent-warning.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:#bf7326; }
      .bp3-button.bp3-outlined.bp3-intent-warning:hover{
        background:rgba(217, 130, 43, 0.15);
        color:#bf7326; }
      .bp3-button.bp3-outlined.bp3-intent-warning:active, .bp3-button.bp3-outlined.bp3-intent-warning.bp3-active{
        background:rgba(217, 130, 43, 0.3);
        color:#bf7326; }
      .bp3-button.bp3-outlined.bp3-intent-warning:disabled, .bp3-button.bp3-outlined.bp3-intent-warning.bp3-disabled{
        background:none;
        color:rgba(191, 115, 38, 0.5); }
        .bp3-button.bp3-outlined.bp3-intent-warning:disabled.bp3-active, .bp3-button.bp3-outlined.bp3-intent-warning.bp3-disabled.bp3-active{
          background:rgba(217, 130, 43, 0.3); }
      .bp3-button.bp3-outlined.bp3-intent-warning .bp3-button-spinner .bp3-spinner-head{
        stroke:#bf7326; }
      .bp3-dark .bp3-button.bp3-outlined.bp3-intent-warning{
        color:#ffb366; }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-warning:hover{
          background:rgba(217, 130, 43, 0.2);
          color:#ffb366; }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-warning:active, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-warning.bp3-active{
          background:rgba(217, 130, 43, 0.3);
          color:#ffb366; }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-warning:disabled, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-warning.bp3-disabled{
          background:none;
          color:rgba(255, 179, 102, 0.5); }
          .bp3-dark .bp3-button.bp3-outlined.bp3-intent-warning:disabled.bp3-active, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-warning.bp3-disabled.bp3-active{
            background:rgba(217, 130, 43, 0.3); }
    .bp3-button.bp3-outlined.bp3-intent-danger{
      color:#c23030; }
      .bp3-button.bp3-outlined.bp3-intent-danger:hover, .bp3-button.bp3-outlined.bp3-intent-danger:active, .bp3-button.bp3-outlined.bp3-intent-danger.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:#c23030; }
      .bp3-button.bp3-outlined.bp3-intent-danger:hover{
        background:rgba(219, 55, 55, 0.15);
        color:#c23030; }
      .bp3-button.bp3-outlined.bp3-intent-danger:active, .bp3-button.bp3-outlined.bp3-intent-danger.bp3-active{
        background:rgba(219, 55, 55, 0.3);
        color:#c23030; }
      .bp3-button.bp3-outlined.bp3-intent-danger:disabled, .bp3-button.bp3-outlined.bp3-intent-danger.bp3-disabled{
        background:none;
        color:rgba(194, 48, 48, 0.5); }
        .bp3-button.bp3-outlined.bp3-intent-danger:disabled.bp3-active, .bp3-button.bp3-outlined.bp3-intent-danger.bp3-disabled.bp3-active{
          background:rgba(219, 55, 55, 0.3); }
      .bp3-button.bp3-outlined.bp3-intent-danger .bp3-button-spinner .bp3-spinner-head{
        stroke:#c23030; }
      .bp3-dark .bp3-button.bp3-outlined.bp3-intent-danger{
        color:#ff7373; }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-danger:hover{
          background:rgba(219, 55, 55, 0.2);
          color:#ff7373; }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-danger:active, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-danger.bp3-active{
          background:rgba(219, 55, 55, 0.3);
          color:#ff7373; }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-danger:disabled, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-danger.bp3-disabled{
          background:none;
          color:rgba(255, 115, 115, 0.5); }
          .bp3-dark .bp3-button.bp3-outlined.bp3-intent-danger:disabled.bp3-active, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-danger.bp3-disabled.bp3-active{
            background:rgba(219, 55, 55, 0.3); }
    .bp3-button.bp3-outlined:disabled, .bp3-button.bp3-outlined.bp3-disabled, .bp3-button.bp3-outlined:disabled:hover, .bp3-button.bp3-outlined.bp3-disabled:hover{
      border-color:rgba(92, 112, 128, 0.1); }
    .bp3-dark .bp3-button.bp3-outlined{
      border-color:rgba(255, 255, 255, 0.4); }
      .bp3-dark .bp3-button.bp3-outlined:disabled, .bp3-dark .bp3-button.bp3-outlined:disabled:hover, .bp3-dark .bp3-button.bp3-outlined.bp3-disabled, .bp3-dark .bp3-button.bp3-outlined.bp3-disabled:hover{
        border-color:rgba(255, 255, 255, 0.2); }
    .bp3-button.bp3-outlined.bp3-intent-primary{
      border-color:rgba(16, 107, 163, 0.6); }
      .bp3-button.bp3-outlined.bp3-intent-primary:disabled, .bp3-button.bp3-outlined.bp3-intent-primary.bp3-disabled{
        border-color:rgba(16, 107, 163, 0.2); }
      .bp3-dark .bp3-button.bp3-outlined.bp3-intent-primary{
        border-color:rgba(72, 175, 240, 0.6); }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-primary:disabled, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-primary.bp3-disabled{
          border-color:rgba(72, 175, 240, 0.2); }
    .bp3-button.bp3-outlined.bp3-intent-success{
      border-color:rgba(13, 128, 80, 0.6); }
      .bp3-button.bp3-outlined.bp3-intent-success:disabled, .bp3-button.bp3-outlined.bp3-intent-success.bp3-disabled{
        border-color:rgba(13, 128, 80, 0.2); }
      .bp3-dark .bp3-button.bp3-outlined.bp3-intent-success{
        border-color:rgba(61, 204, 145, 0.6); }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-success:disabled, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-success.bp3-disabled{
          border-color:rgba(61, 204, 145, 0.2); }
    .bp3-button.bp3-outlined.bp3-intent-warning{
      border-color:rgba(191, 115, 38, 0.6); }
      .bp3-button.bp3-outlined.bp3-intent-warning:disabled, .bp3-button.bp3-outlined.bp3-intent-warning.bp3-disabled{
        border-color:rgba(191, 115, 38, 0.2); }
      .bp3-dark .bp3-button.bp3-outlined.bp3-intent-warning{
        border-color:rgba(255, 179, 102, 0.6); }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-warning:disabled, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-warning.bp3-disabled{
          border-color:rgba(255, 179, 102, 0.2); }
    .bp3-button.bp3-outlined.bp3-intent-danger{
      border-color:rgba(194, 48, 48, 0.6); }
      .bp3-button.bp3-outlined.bp3-intent-danger:disabled, .bp3-button.bp3-outlined.bp3-intent-danger.bp3-disabled{
        border-color:rgba(194, 48, 48, 0.2); }
      .bp3-dark .bp3-button.bp3-outlined.bp3-intent-danger{
        border-color:rgba(255, 115, 115, 0.6); }
        .bp3-dark .bp3-button.bp3-outlined.bp3-intent-danger:disabled, .bp3-dark .bp3-button.bp3-outlined.bp3-intent-danger.bp3-disabled{
          border-color:rgba(255, 115, 115, 0.2); }

a.bp3-button{
  text-align:center;
  text-decoration:none;
  -webkit-transition:none;
  transition:none; }
  a.bp3-button, a.bp3-button:hover, a.bp3-button:active{
    color:#182026; }
  a.bp3-button.bp3-disabled{
    color:rgba(92, 112, 128, 0.6); }

.bp3-button-text{
  -webkit-box-flex:0;
      -ms-flex:0 1 auto;
          flex:0 1 auto; }

.bp3-button.bp3-align-left .bp3-button-text, .bp3-button.bp3-align-right .bp3-button-text,
.bp3-button-group.bp3-align-left .bp3-button-text,
.bp3-button-group.bp3-align-right .bp3-button-text{
  -webkit-box-flex:1;
      -ms-flex:1 1 auto;
          flex:1 1 auto; }
.bp3-button-group{
  display:-webkit-inline-box;
  display:-ms-inline-flexbox;
  display:inline-flex; }
  .bp3-button-group .bp3-button{
    -webkit-box-flex:0;
        -ms-flex:0 0 auto;
            flex:0 0 auto;
    position:relative;
    z-index:4; }
    .bp3-button-group .bp3-button:focus{
      z-index:5; }
    .bp3-button-group .bp3-button:hover{
      z-index:6; }
    .bp3-button-group .bp3-button:active, .bp3-button-group .bp3-button.bp3-active{
      z-index:7; }
    .bp3-button-group .bp3-button:disabled, .bp3-button-group .bp3-button.bp3-disabled{
      z-index:3; }
    .bp3-button-group .bp3-button[class*="bp3-intent-"]{
      z-index:9; }
      .bp3-button-group .bp3-button[class*="bp3-intent-"]:focus{
        z-index:10; }
      .bp3-button-group .bp3-button[class*="bp3-intent-"]:hover{
        z-index:11; }
      .bp3-button-group .bp3-button[class*="bp3-intent-"]:active, .bp3-button-group .bp3-button[class*="bp3-intent-"].bp3-active{
        z-index:12; }
      .bp3-button-group .bp3-button[class*="bp3-intent-"]:disabled, .bp3-button-group .bp3-button[class*="bp3-intent-"].bp3-disabled{
        z-index:8; }
  .bp3-button-group:not(.bp3-minimal) > .bp3-popover-wrapper:not(:first-child) .bp3-button,
  .bp3-button-group:not(.bp3-minimal) > .bp3-button:not(:first-child){
    border-bottom-left-radius:0;
    border-top-left-radius:0; }
  .bp3-button-group:not(.bp3-minimal) > .bp3-popover-wrapper:not(:last-child) .bp3-button,
  .bp3-button-group:not(.bp3-minimal) > .bp3-button:not(:last-child){
    border-bottom-right-radius:0;
    border-top-right-radius:0;
    margin-right:-1px; }
  .bp3-button-group.bp3-minimal .bp3-button{
    background:none;
    -webkit-box-shadow:none;
            box-shadow:none; }
    .bp3-button-group.bp3-minimal .bp3-button:hover{
      background:rgba(167, 182, 194, 0.3);
      -webkit-box-shadow:none;
              box-shadow:none;
      color:#182026;
      text-decoration:none; }
    .bp3-button-group.bp3-minimal .bp3-button:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-active{
      background:rgba(115, 134, 148, 0.3);
      -webkit-box-shadow:none;
              box-shadow:none;
      color:#182026; }
    .bp3-button-group.bp3-minimal .bp3-button:disabled, .bp3-button-group.bp3-minimal .bp3-button:disabled:hover, .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled, .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled:hover{
      background:none;
      color:rgba(92, 112, 128, 0.6);
      cursor:not-allowed; }
      .bp3-button-group.bp3-minimal .bp3-button:disabled.bp3-active, .bp3-button-group.bp3-minimal .bp3-button:disabled:hover.bp3-active, .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled.bp3-active, .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled:hover.bp3-active{
        background:rgba(115, 134, 148, 0.3); }
    .bp3-dark .bp3-button-group.bp3-minimal .bp3-button{
      background:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:inherit; }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:hover, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none; }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:hover{
        background:rgba(138, 155, 168, 0.15); }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-active{
        background:rgba(138, 155, 168, 0.3);
        color:#f5f8fa; }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:disabled, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:disabled:hover, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled:hover{
        background:none;
        color:rgba(167, 182, 194, 0.6);
        cursor:not-allowed; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:disabled.bp3-active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:disabled:hover.bp3-active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled.bp3-active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled:hover.bp3-active{
          background:rgba(138, 155, 168, 0.3); }
    .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary{
      color:#106ba3; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:hover, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:#106ba3; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:hover{
        background:rgba(19, 124, 189, 0.15);
        color:#106ba3; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary.bp3-active{
        background:rgba(19, 124, 189, 0.3);
        color:#106ba3; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:disabled, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary.bp3-disabled{
        background:none;
        color:rgba(16, 107, 163, 0.5); }
        .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:disabled.bp3-active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary.bp3-disabled.bp3-active{
          background:rgba(19, 124, 189, 0.3); }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary .bp3-button-spinner .bp3-spinner-head{
        stroke:#106ba3; }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary{
        color:#48aff0; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:hover{
          background:rgba(19, 124, 189, 0.2);
          color:#48aff0; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary.bp3-active{
          background:rgba(19, 124, 189, 0.3);
          color:#48aff0; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:disabled, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary.bp3-disabled{
          background:none;
          color:rgba(72, 175, 240, 0.5); }
          .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:disabled.bp3-active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary.bp3-disabled.bp3-active{
            background:rgba(19, 124, 189, 0.3); }
    .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success{
      color:#0d8050; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:hover, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:#0d8050; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:hover{
        background:rgba(15, 153, 96, 0.15);
        color:#0d8050; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success.bp3-active{
        background:rgba(15, 153, 96, 0.3);
        color:#0d8050; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:disabled, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success.bp3-disabled{
        background:none;
        color:rgba(13, 128, 80, 0.5); }
        .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:disabled.bp3-active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success.bp3-disabled.bp3-active{
          background:rgba(15, 153, 96, 0.3); }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success .bp3-button-spinner .bp3-spinner-head{
        stroke:#0d8050; }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success{
        color:#3dcc91; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:hover{
          background:rgba(15, 153, 96, 0.2);
          color:#3dcc91; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success.bp3-active{
          background:rgba(15, 153, 96, 0.3);
          color:#3dcc91; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:disabled, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success.bp3-disabled{
          background:none;
          color:rgba(61, 204, 145, 0.5); }
          .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:disabled.bp3-active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success.bp3-disabled.bp3-active{
            background:rgba(15, 153, 96, 0.3); }
    .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning{
      color:#bf7326; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:hover, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:#bf7326; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:hover{
        background:rgba(217, 130, 43, 0.15);
        color:#bf7326; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning.bp3-active{
        background:rgba(217, 130, 43, 0.3);
        color:#bf7326; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:disabled, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning.bp3-disabled{
        background:none;
        color:rgba(191, 115, 38, 0.5); }
        .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:disabled.bp3-active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning.bp3-disabled.bp3-active{
          background:rgba(217, 130, 43, 0.3); }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning .bp3-button-spinner .bp3-spinner-head{
        stroke:#bf7326; }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning{
        color:#ffb366; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:hover{
          background:rgba(217, 130, 43, 0.2);
          color:#ffb366; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning.bp3-active{
          background:rgba(217, 130, 43, 0.3);
          color:#ffb366; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:disabled, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning.bp3-disabled{
          background:none;
          color:rgba(255, 179, 102, 0.5); }
          .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:disabled.bp3-active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning.bp3-disabled.bp3-active{
            background:rgba(217, 130, 43, 0.3); }
    .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger{
      color:#c23030; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:hover, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger.bp3-active{
        background:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:#c23030; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:hover{
        background:rgba(219, 55, 55, 0.15);
        color:#c23030; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger.bp3-active{
        background:rgba(219, 55, 55, 0.3);
        color:#c23030; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:disabled, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger.bp3-disabled{
        background:none;
        color:rgba(194, 48, 48, 0.5); }
        .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:disabled.bp3-active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger.bp3-disabled.bp3-active{
          background:rgba(219, 55, 55, 0.3); }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger .bp3-button-spinner .bp3-spinner-head{
        stroke:#c23030; }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger{
        color:#ff7373; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:hover{
          background:rgba(219, 55, 55, 0.2);
          color:#ff7373; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger.bp3-active{
          background:rgba(219, 55, 55, 0.3);
          color:#ff7373; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:disabled, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger.bp3-disabled{
          background:none;
          color:rgba(255, 115, 115, 0.5); }
          .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:disabled.bp3-active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger.bp3-disabled.bp3-active{
            background:rgba(219, 55, 55, 0.3); }
  .bp3-button-group .bp3-popover-wrapper,
  .bp3-button-group .bp3-popover-target{
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto; }
  .bp3-button-group.bp3-fill{
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    width:100%; }
  .bp3-button-group .bp3-button.bp3-fill,
  .bp3-button-group.bp3-fill .bp3-button:not(.bp3-fixed){
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto; }
  .bp3-button-group.bp3-vertical{
    -webkit-box-align:stretch;
        -ms-flex-align:stretch;
            align-items:stretch;
    -webkit-box-orient:vertical;
    -webkit-box-direction:normal;
        -ms-flex-direction:column;
            flex-direction:column;
    vertical-align:top; }
    .bp3-button-group.bp3-vertical.bp3-fill{
      height:100%;
      width:unset; }
    .bp3-button-group.bp3-vertical .bp3-button{
      margin-right:0 !important;
      width:100%; }
    .bp3-button-group.bp3-vertical:not(.bp3-minimal) > .bp3-popover-wrapper:first-child .bp3-button,
    .bp3-button-group.bp3-vertical:not(.bp3-minimal) > .bp3-button:first-child{
      border-radius:3px 3px 0 0; }
    .bp3-button-group.bp3-vertical:not(.bp3-minimal) > .bp3-popover-wrapper:last-child .bp3-button,
    .bp3-button-group.bp3-vertical:not(.bp3-minimal) > .bp3-button:last-child{
      border-radius:0 0 3px 3px; }
    .bp3-button-group.bp3-vertical:not(.bp3-minimal) > .bp3-popover-wrapper:not(:last-child) .bp3-button,
    .bp3-button-group.bp3-vertical:not(.bp3-minimal) > .bp3-button:not(:last-child){
      margin-bottom:-1px; }
  .bp3-button-group.bp3-align-left .bp3-button{
    text-align:left; }
  .bp3-dark .bp3-button-group:not(.bp3-minimal) > .bp3-popover-wrapper:not(:last-child) .bp3-button,
  .bp3-dark .bp3-button-group:not(.bp3-minimal) > .bp3-button:not(:last-child){
    margin-right:1px; }
  .bp3-dark .bp3-button-group.bp3-vertical > .bp3-popover-wrapper:not(:last-child) .bp3-button,
  .bp3-dark .bp3-button-group.bp3-vertical > .bp3-button:not(:last-child){
    margin-bottom:1px; }
.bp3-callout{
  font-size:14px;
  line-height:1.5;
  background-color:rgba(138, 155, 168, 0.15);
  border-radius:3px;
  padding:10px 12px 9px;
  position:relative;
  width:100%; }
  .bp3-callout[class*="bp3-icon-"]{
    padding-left:40px; }
    .bp3-callout[class*="bp3-icon-"]::before{
      font-family:"Icons20", sans-serif;
      font-size:20px;
      font-style:normal;
      font-weight:400;
      line-height:1;
      -moz-osx-font-smoothing:grayscale;
      -webkit-font-smoothing:antialiased;
      color:#5c7080;
      left:10px;
      position:absolute;
      top:10px; }
  .bp3-callout.bp3-callout-icon{
    padding-left:40px; }
    .bp3-callout.bp3-callout-icon > .bp3-icon:first-child{
      color:#5c7080;
      left:10px;
      position:absolute;
      top:10px; }
  .bp3-callout .bp3-heading{
    line-height:20px;
    margin-bottom:5px;
    margin-top:0; }
    .bp3-callout .bp3-heading:last-child{
      margin-bottom:0; }
  .bp3-dark .bp3-callout{
    background-color:rgba(138, 155, 168, 0.2); }
    .bp3-dark .bp3-callout[class*="bp3-icon-"]::before{
      color:#a7b6c2; }
  .bp3-callout.bp3-intent-primary{
    background-color:rgba(19, 124, 189, 0.15); }
    .bp3-callout.bp3-intent-primary[class*="bp3-icon-"]::before,
    .bp3-callout.bp3-intent-primary > .bp3-icon:first-child,
    .bp3-callout.bp3-intent-primary .bp3-heading{
      color:#106ba3; }
    .bp3-dark .bp3-callout.bp3-intent-primary{
      background-color:rgba(19, 124, 189, 0.25); }
      .bp3-dark .bp3-callout.bp3-intent-primary[class*="bp3-icon-"]::before,
      .bp3-dark .bp3-callout.bp3-intent-primary > .bp3-icon:first-child,
      .bp3-dark .bp3-callout.bp3-intent-primary .bp3-heading{
        color:#48aff0; }
  .bp3-callout.bp3-intent-success{
    background-color:rgba(15, 153, 96, 0.15); }
    .bp3-callout.bp3-intent-success[class*="bp3-icon-"]::before,
    .bp3-callout.bp3-intent-success > .bp3-icon:first-child,
    .bp3-callout.bp3-intent-success .bp3-heading{
      color:#0d8050; }
    .bp3-dark .bp3-callout.bp3-intent-success{
      background-color:rgba(15, 153, 96, 0.25); }
      .bp3-dark .bp3-callout.bp3-intent-success[class*="bp3-icon-"]::before,
      .bp3-dark .bp3-callout.bp3-intent-success > .bp3-icon:first-child,
      .bp3-dark .bp3-callout.bp3-intent-success .bp3-heading{
        color:#3dcc91; }
  .bp3-callout.bp3-intent-warning{
    background-color:rgba(217, 130, 43, 0.15); }
    .bp3-callout.bp3-intent-warning[class*="bp3-icon-"]::before,
    .bp3-callout.bp3-intent-warning > .bp3-icon:first-child,
    .bp3-callout.bp3-intent-warning .bp3-heading{
      color:#bf7326; }
    .bp3-dark .bp3-callout.bp3-intent-warning{
      background-color:rgba(217, 130, 43, 0.25); }
      .bp3-dark .bp3-callout.bp3-intent-warning[class*="bp3-icon-"]::before,
      .bp3-dark .bp3-callout.bp3-intent-warning > .bp3-icon:first-child,
      .bp3-dark .bp3-callout.bp3-intent-warning .bp3-heading{
        color:#ffb366; }
  .bp3-callout.bp3-intent-danger{
    background-color:rgba(219, 55, 55, 0.15); }
    .bp3-callout.bp3-intent-danger[class*="bp3-icon-"]::before,
    .bp3-callout.bp3-intent-danger > .bp3-icon:first-child,
    .bp3-callout.bp3-intent-danger .bp3-heading{
      color:#c23030; }
    .bp3-dark .bp3-callout.bp3-intent-danger{
      background-color:rgba(219, 55, 55, 0.25); }
      .bp3-dark .bp3-callout.bp3-intent-danger[class*="bp3-icon-"]::before,
      .bp3-dark .bp3-callout.bp3-intent-danger > .bp3-icon:first-child,
      .bp3-dark .bp3-callout.bp3-intent-danger .bp3-heading{
        color:#ff7373; }
  .bp3-running-text .bp3-callout{
    margin:20px 0; }
.bp3-card{
  background-color:#ffffff;
  border-radius:3px;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.15), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.15), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0);
  padding:20px;
  -webkit-transition:-webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:-webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9), box-shadow 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9), box-shadow 200ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 200ms cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-card.bp3-dark,
  .bp3-dark .bp3-card{
    background-color:#30404d;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0); }

.bp3-elevation-0{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.15), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.15), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0); }
  .bp3-elevation-0.bp3-dark,
  .bp3-dark .bp3-elevation-0{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0); }

.bp3-elevation-1{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-elevation-1.bp3-dark,
  .bp3-dark .bp3-elevation-1{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4); }

.bp3-elevation-2{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 1px 1px rgba(16, 22, 26, 0.2), 0 2px 6px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 1px 1px rgba(16, 22, 26, 0.2), 0 2px 6px rgba(16, 22, 26, 0.2); }
  .bp3-elevation-2.bp3-dark,
  .bp3-dark .bp3-elevation-2{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.4), 0 2px 6px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.4), 0 2px 6px rgba(16, 22, 26, 0.4); }

.bp3-elevation-3{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2); }
  .bp3-elevation-3.bp3-dark,
  .bp3-dark .bp3-elevation-3{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4); }

.bp3-elevation-4{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2); }
  .bp3-elevation-4.bp3-dark,
  .bp3-dark .bp3-elevation-4{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4); }

.bp3-card.bp3-interactive:hover{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
  cursor:pointer; }
  .bp3-card.bp3-interactive:hover.bp3-dark,
  .bp3-dark .bp3-card.bp3-interactive:hover{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4); }

.bp3-card.bp3-interactive:active{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2);
  opacity:0.9;
  -webkit-transition-duration:0;
          transition-duration:0; }
  .bp3-card.bp3-interactive:active.bp3-dark,
  .bp3-dark .bp3-card.bp3-interactive:active{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4); }

.bp3-collapse{
  height:0;
  overflow-y:hidden;
  -webkit-transition:height 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:height 200ms cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-collapse .bp3-collapse-body{
    -webkit-transition:-webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:-webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9); }
    .bp3-collapse .bp3-collapse-body[aria-hidden="true"]{
      display:none; }

.bp3-context-menu .bp3-popover-target{
  display:block; }

.bp3-context-menu-popover-target{
  position:fixed; }

.bp3-divider{
  border-bottom:1px solid rgba(16, 22, 26, 0.15);
  border-right:1px solid rgba(16, 22, 26, 0.15);
  margin:5px; }
  .bp3-dark .bp3-divider{
    border-color:rgba(16, 22, 26, 0.4); }
.bp3-dialog-container{
  opacity:1;
  -webkit-transform:scale(1);
          transform:scale(1);
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-pack:center;
      -ms-flex-pack:center;
          justify-content:center;
  min-height:100%;
  pointer-events:none;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none;
  width:100%; }
  .bp3-dialog-container.bp3-overlay-enter > .bp3-dialog, .bp3-dialog-container.bp3-overlay-appear > .bp3-dialog{
    opacity:0;
    -webkit-transform:scale(0.5);
            transform:scale(0.5); }
  .bp3-dialog-container.bp3-overlay-enter-active > .bp3-dialog, .bp3-dialog-container.bp3-overlay-appear-active > .bp3-dialog{
    opacity:1;
    -webkit-transform:scale(1);
            transform:scale(1);
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:300ms;
            transition-duration:300ms;
    -webkit-transition-property:opacity, -webkit-transform;
    transition-property:opacity, -webkit-transform;
    transition-property:opacity, transform;
    transition-property:opacity, transform, -webkit-transform;
    -webkit-transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
            transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11); }
  .bp3-dialog-container.bp3-overlay-exit > .bp3-dialog{
    opacity:1;
    -webkit-transform:scale(1);
            transform:scale(1); }
  .bp3-dialog-container.bp3-overlay-exit-active > .bp3-dialog{
    opacity:0;
    -webkit-transform:scale(0.5);
            transform:scale(0.5);
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:300ms;
            transition-duration:300ms;
    -webkit-transition-property:opacity, -webkit-transform;
    transition-property:opacity, -webkit-transform;
    transition-property:opacity, transform;
    transition-property:opacity, transform, -webkit-transform;
    -webkit-transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
            transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11); }

.bp3-dialog{
  background:#ebf1f5;
  border-radius:6px;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2);
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:vertical;
  -webkit-box-direction:normal;
      -ms-flex-direction:column;
          flex-direction:column;
  margin:30px 0;
  padding-bottom:20px;
  pointer-events:all;
  -webkit-user-select:text;
     -moz-user-select:text;
      -ms-user-select:text;
          user-select:text;
  width:500px; }
  .bp3-dialog:focus{
    outline:0; }
  .bp3-dialog.bp3-dark,
  .bp3-dark .bp3-dialog{
    background:#293742;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4);
    color:#f5f8fa; }

.bp3-dialog-header{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  background:#ffffff;
  border-radius:6px 6px 0 0;
  -webkit-box-shadow:0 1px 0 rgba(16, 22, 26, 0.15);
          box-shadow:0 1px 0 rgba(16, 22, 26, 0.15);
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-flex:0;
      -ms-flex:0 0 auto;
          flex:0 0 auto;
  min-height:40px;
  padding-left:20px;
  padding-right:5px;
  z-index:30; }
  .bp3-dialog-header .bp3-icon-large,
  .bp3-dialog-header .bp3-icon{
    color:#5c7080;
    -webkit-box-flex:0;
        -ms-flex:0 0 auto;
            flex:0 0 auto;
    margin-right:10px; }
  .bp3-dialog-header .bp3-heading{
    overflow:hidden;
    text-overflow:ellipsis;
    white-space:nowrap;
    word-wrap:normal;
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto;
    line-height:inherit;
    margin:0; }
    .bp3-dialog-header .bp3-heading:last-child{
      margin-right:20px; }
  .bp3-dark .bp3-dialog-header{
    background:#30404d;
    -webkit-box-shadow:0 1px 0 rgba(16, 22, 26, 0.4);
            box-shadow:0 1px 0 rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-dialog-header .bp3-icon-large,
    .bp3-dark .bp3-dialog-header .bp3-icon{
      color:#a7b6c2; }

.bp3-dialog-body{
  -webkit-box-flex:1;
      -ms-flex:1 1 auto;
          flex:1 1 auto;
  line-height:18px;
  margin:20px; }

.bp3-dialog-footer{
  -webkit-box-flex:0;
      -ms-flex:0 0 auto;
          flex:0 0 auto;
  margin:0 20px; }

.bp3-dialog-footer-actions{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-pack:end;
      -ms-flex-pack:end;
          justify-content:flex-end; }
  .bp3-dialog-footer-actions .bp3-button{
    margin-left:10px; }
.bp3-multistep-dialog-panels{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex; }

.bp3-multistep-dialog-left-panel{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-flex:1;
      -ms-flex:1;
          flex:1;
  -webkit-box-orient:vertical;
  -webkit-box-direction:normal;
      -ms-flex-direction:column;
          flex-direction:column; }
  .bp3-dark .bp3-multistep-dialog-left-panel{
    background:#202b33; }

.bp3-multistep-dialog-right-panel{
  background-color:#f5f8fa;
  border-left:1px solid rgba(16, 22, 26, 0.15);
  border-radius:0 0 6px 0;
  -webkit-box-flex:3;
      -ms-flex:3;
          flex:3;
  min-width:0; }
  .bp3-dark .bp3-multistep-dialog-right-panel{
    background-color:#293742;
    border-left:1px solid rgba(16, 22, 26, 0.4); }

.bp3-multistep-dialog-footer{
  background-color:#ffffff;
  border-radius:0 0 6px 0;
  border-top:1px solid rgba(16, 22, 26, 0.15);
  padding:10px; }
  .bp3-dark .bp3-multistep-dialog-footer{
    background:#30404d;
    border-top:1px solid rgba(16, 22, 26, 0.4); }

.bp3-dialog-step-container{
  background-color:#f5f8fa;
  border-bottom:1px solid rgba(16, 22, 26, 0.15); }
  .bp3-dark .bp3-dialog-step-container{
    background:#293742;
    border-bottom:1px solid rgba(16, 22, 26, 0.4); }
  .bp3-dialog-step-container.bp3-dialog-step-viewed{
    background-color:#ffffff; }
    .bp3-dark .bp3-dialog-step-container.bp3-dialog-step-viewed{
      background:#30404d; }

.bp3-dialog-step{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  background-color:#f5f8fa;
  border-radius:6px;
  cursor:not-allowed;
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  margin:4px;
  padding:6px 14px; }
  .bp3-dark .bp3-dialog-step{
    background:#293742; }
  .bp3-dialog-step-viewed .bp3-dialog-step{
    background-color:#ffffff;
    cursor:pointer; }
    .bp3-dark .bp3-dialog-step-viewed .bp3-dialog-step{
      background:#30404d; }
  .bp3-dialog-step:hover{
    background-color:#f5f8fa; }
    .bp3-dark .bp3-dialog-step:hover{
      background:#293742; }

.bp3-dialog-step-icon{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  background-color:rgba(92, 112, 128, 0.6);
  border-radius:50%;
  color:#ffffff;
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  height:25px;
  -webkit-box-pack:center;
      -ms-flex-pack:center;
          justify-content:center;
  width:25px; }
  .bp3-dark .bp3-dialog-step-icon{
    background-color:rgba(167, 182, 194, 0.6); }
  .bp3-active.bp3-dialog-step-viewed .bp3-dialog-step-icon{
    background-color:#2b95d6; }
  .bp3-dialog-step-viewed .bp3-dialog-step-icon{
    background-color:#8a9ba8; }

.bp3-dialog-step-title{
  color:rgba(92, 112, 128, 0.6);
  -webkit-box-flex:1;
      -ms-flex:1;
          flex:1;
  padding-left:10px; }
  .bp3-dark .bp3-dialog-step-title{
    color:rgba(167, 182, 194, 0.6); }
  .bp3-active.bp3-dialog-step-viewed .bp3-dialog-step-title{
    color:#2b95d6; }
  .bp3-dialog-step-viewed:not(.bp3-active) .bp3-dialog-step-title{
    color:#182026; }
    .bp3-dark .bp3-dialog-step-viewed:not(.bp3-active) .bp3-dialog-step-title{
      color:#f5f8fa; }
.bp3-drawer{
  background:#ffffff;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2);
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:vertical;
  -webkit-box-direction:normal;
      -ms-flex-direction:column;
          flex-direction:column;
  margin:0;
  padding:0; }
  .bp3-drawer:focus{
    outline:0; }
  .bp3-drawer.bp3-position-top{
    height:50%;
    left:0;
    right:0;
    top:0; }
    .bp3-drawer.bp3-position-top.bp3-overlay-enter, .bp3-drawer.bp3-position-top.bp3-overlay-appear{
      -webkit-transform:translateY(-100%);
              transform:translateY(-100%); }
    .bp3-drawer.bp3-position-top.bp3-overlay-enter-active, .bp3-drawer.bp3-position-top.bp3-overlay-appear-active{
      -webkit-transform:translateY(0);
              transform:translateY(0);
      -webkit-transition-delay:0;
              transition-delay:0;
      -webkit-transition-duration:200ms;
              transition-duration:200ms;
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
    .bp3-drawer.bp3-position-top.bp3-overlay-exit{
      -webkit-transform:translateY(0);
              transform:translateY(0); }
    .bp3-drawer.bp3-position-top.bp3-overlay-exit-active{
      -webkit-transform:translateY(-100%);
              transform:translateY(-100%);
      -webkit-transition-delay:0;
              transition-delay:0;
      -webkit-transition-duration:100ms;
              transition-duration:100ms;
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-drawer.bp3-position-bottom{
    bottom:0;
    height:50%;
    left:0;
    right:0; }
    .bp3-drawer.bp3-position-bottom.bp3-overlay-enter, .bp3-drawer.bp3-position-bottom.bp3-overlay-appear{
      -webkit-transform:translateY(100%);
              transform:translateY(100%); }
    .bp3-drawer.bp3-position-bottom.bp3-overlay-enter-active, .bp3-drawer.bp3-position-bottom.bp3-overlay-appear-active{
      -webkit-transform:translateY(0);
              transform:translateY(0);
      -webkit-transition-delay:0;
              transition-delay:0;
      -webkit-transition-duration:200ms;
              transition-duration:200ms;
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
    .bp3-drawer.bp3-position-bottom.bp3-overlay-exit{
      -webkit-transform:translateY(0);
              transform:translateY(0); }
    .bp3-drawer.bp3-position-bottom.bp3-overlay-exit-active{
      -webkit-transform:translateY(100%);
              transform:translateY(100%);
      -webkit-transition-delay:0;
              transition-delay:0;
      -webkit-transition-duration:100ms;
              transition-duration:100ms;
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-drawer.bp3-position-left{
    bottom:0;
    left:0;
    top:0;
    width:50%; }
    .bp3-drawer.bp3-position-left.bp3-overlay-enter, .bp3-drawer.bp3-position-left.bp3-overlay-appear{
      -webkit-transform:translateX(-100%);
              transform:translateX(-100%); }
    .bp3-drawer.bp3-position-left.bp3-overlay-enter-active, .bp3-drawer.bp3-position-left.bp3-overlay-appear-active{
      -webkit-transform:translateX(0);
              transform:translateX(0);
      -webkit-transition-delay:0;
              transition-delay:0;
      -webkit-transition-duration:200ms;
              transition-duration:200ms;
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
    .bp3-drawer.bp3-position-left.bp3-overlay-exit{
      -webkit-transform:translateX(0);
              transform:translateX(0); }
    .bp3-drawer.bp3-position-left.bp3-overlay-exit-active{
      -webkit-transform:translateX(-100%);
              transform:translateX(-100%);
      -webkit-transition-delay:0;
              transition-delay:0;
      -webkit-transition-duration:100ms;
              transition-duration:100ms;
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-drawer.bp3-position-right{
    bottom:0;
    right:0;
    top:0;
    width:50%; }
    .bp3-drawer.bp3-position-right.bp3-overlay-enter, .bp3-drawer.bp3-position-right.bp3-overlay-appear{
      -webkit-transform:translateX(100%);
              transform:translateX(100%); }
    .bp3-drawer.bp3-position-right.bp3-overlay-enter-active, .bp3-drawer.bp3-position-right.bp3-overlay-appear-active{
      -webkit-transform:translateX(0);
              transform:translateX(0);
      -webkit-transition-delay:0;
              transition-delay:0;
      -webkit-transition-duration:200ms;
              transition-duration:200ms;
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
    .bp3-drawer.bp3-position-right.bp3-overlay-exit{
      -webkit-transform:translateX(0);
              transform:translateX(0); }
    .bp3-drawer.bp3-position-right.bp3-overlay-exit-active{
      -webkit-transform:translateX(100%);
              transform:translateX(100%);
      -webkit-transition-delay:0;
              transition-delay:0;
      -webkit-transition-duration:100ms;
              transition-duration:100ms;
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
  .bp3-position-right):not(.bp3-vertical){
    bottom:0;
    right:0;
    top:0;
    width:50%; }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right):not(.bp3-vertical).bp3-overlay-enter, .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right):not(.bp3-vertical).bp3-overlay-appear{
      -webkit-transform:translateX(100%);
              transform:translateX(100%); }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right):not(.bp3-vertical).bp3-overlay-enter-active, .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right):not(.bp3-vertical).bp3-overlay-appear-active{
      -webkit-transform:translateX(0);
              transform:translateX(0);
      -webkit-transition-delay:0;
              transition-delay:0;
      -webkit-transition-duration:200ms;
              transition-duration:200ms;
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right):not(.bp3-vertical).bp3-overlay-exit{
      -webkit-transform:translateX(0);
              transform:translateX(0); }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right):not(.bp3-vertical).bp3-overlay-exit-active{
      -webkit-transform:translateX(100%);
              transform:translateX(100%);
      -webkit-transition-delay:0;
              transition-delay:0;
      -webkit-transition-duration:100ms;
              transition-duration:100ms;
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
  .bp3-position-right).bp3-vertical{
    bottom:0;
    height:50%;
    left:0;
    right:0; }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right).bp3-vertical.bp3-overlay-enter, .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right).bp3-vertical.bp3-overlay-appear{
      -webkit-transform:translateY(100%);
              transform:translateY(100%); }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right).bp3-vertical.bp3-overlay-enter-active, .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right).bp3-vertical.bp3-overlay-appear-active{
      -webkit-transform:translateY(0);
              transform:translateY(0);
      -webkit-transition-delay:0;
              transition-delay:0;
      -webkit-transition-duration:200ms;
              transition-duration:200ms;
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right).bp3-vertical.bp3-overlay-exit{
      -webkit-transform:translateY(0);
              transform:translateY(0); }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right).bp3-vertical.bp3-overlay-exit-active{
      -webkit-transform:translateY(100%);
              transform:translateY(100%);
      -webkit-transition-delay:0;
              transition-delay:0;
      -webkit-transition-duration:100ms;
              transition-duration:100ms;
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-drawer.bp3-dark,
  .bp3-dark .bp3-drawer{
    background:#30404d;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4);
    color:#f5f8fa; }

.bp3-drawer-header{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  border-radius:0;
  -webkit-box-shadow:0 1px 0 rgba(16, 22, 26, 0.15);
          box-shadow:0 1px 0 rgba(16, 22, 26, 0.15);
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-flex:0;
      -ms-flex:0 0 auto;
          flex:0 0 auto;
  min-height:40px;
  padding:5px;
  padding-left:20px;
  position:relative; }
  .bp3-drawer-header .bp3-icon-large,
  .bp3-drawer-header .bp3-icon{
    color:#5c7080;
    -webkit-box-flex:0;
        -ms-flex:0 0 auto;
            flex:0 0 auto;
    margin-right:10px; }
  .bp3-drawer-header .bp3-heading{
    overflow:hidden;
    text-overflow:ellipsis;
    white-space:nowrap;
    word-wrap:normal;
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto;
    line-height:inherit;
    margin:0; }
    .bp3-drawer-header .bp3-heading:last-child{
      margin-right:20px; }
  .bp3-dark .bp3-drawer-header{
    -webkit-box-shadow:0 1px 0 rgba(16, 22, 26, 0.4);
            box-shadow:0 1px 0 rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-drawer-header .bp3-icon-large,
    .bp3-dark .bp3-drawer-header .bp3-icon{
      color:#a7b6c2; }

.bp3-drawer-body{
  -webkit-box-flex:1;
      -ms-flex:1 1 auto;
          flex:1 1 auto;
  line-height:18px;
  overflow:auto; }

.bp3-drawer-footer{
  -webkit-box-shadow:inset 0 1px 0 rgba(16, 22, 26, 0.15);
          box-shadow:inset 0 1px 0 rgba(16, 22, 26, 0.15);
  -webkit-box-flex:0;
      -ms-flex:0 0 auto;
          flex:0 0 auto;
  padding:10px 20px;
  position:relative; }
  .bp3-dark .bp3-drawer-footer{
    -webkit-box-shadow:inset 0 1px 0 rgba(16, 22, 26, 0.4);
            box-shadow:inset 0 1px 0 rgba(16, 22, 26, 0.4); }
.bp3-editable-text{
  cursor:text;
  display:inline-block;
  max-width:100%;
  position:relative;
  vertical-align:top;
  white-space:nowrap; }
  .bp3-editable-text::before{
    bottom:-3px;
    left:-3px;
    position:absolute;
    right:-3px;
    top:-3px;
    border-radius:3px;
    content:"";
    -webkit-transition:background-color 100ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:background-color 100ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:background-color 100ms cubic-bezier(0.4, 1, 0.75, 0.9), box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:background-color 100ms cubic-bezier(0.4, 1, 0.75, 0.9), box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-editable-text:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.15);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.15); }
  .bp3-editable-text.bp3-editable-text-editing::before{
    background-color:#ffffff;
    -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-editable-text.bp3-disabled::before{
    -webkit-box-shadow:none;
            box-shadow:none; }
  .bp3-editable-text.bp3-intent-primary .bp3-editable-text-input,
  .bp3-editable-text.bp3-intent-primary .bp3-editable-text-content{
    color:#137cbd; }
  .bp3-editable-text.bp3-intent-primary:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(19, 124, 189, 0.4);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(19, 124, 189, 0.4); }
  .bp3-editable-text.bp3-intent-primary.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-editable-text.bp3-intent-success .bp3-editable-text-input,
  .bp3-editable-text.bp3-intent-success .bp3-editable-text-content{
    color:#0f9960; }
  .bp3-editable-text.bp3-intent-success:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px rgba(15, 153, 96, 0.4);
            box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px rgba(15, 153, 96, 0.4); }
  .bp3-editable-text.bp3-intent-success.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-editable-text.bp3-intent-warning .bp3-editable-text-input,
  .bp3-editable-text.bp3-intent-warning .bp3-editable-text-content{
    color:#d9822b; }
  .bp3-editable-text.bp3-intent-warning:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px rgba(217, 130, 43, 0.4);
            box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px rgba(217, 130, 43, 0.4); }
  .bp3-editable-text.bp3-intent-warning.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-editable-text.bp3-intent-danger .bp3-editable-text-input,
  .bp3-editable-text.bp3-intent-danger .bp3-editable-text-content{
    color:#db3737; }
  .bp3-editable-text.bp3-intent-danger:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px rgba(219, 55, 55, 0.4);
            box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px rgba(219, 55, 55, 0.4); }
  .bp3-editable-text.bp3-intent-danger.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-dark .bp3-editable-text:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(255, 255, 255, 0.15);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(255, 255, 255, 0.15); }
  .bp3-dark .bp3-editable-text.bp3-editable-text-editing::before{
    background-color:rgba(16, 22, 26, 0.3);
    -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-disabled::before{
    -webkit-box-shadow:none;
            box-shadow:none; }
  .bp3-dark .bp3-editable-text.bp3-intent-primary .bp3-editable-text-content{
    color:#48aff0; }
  .bp3-dark .bp3-editable-text.bp3-intent-primary:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(72, 175, 240, 0), 0 0 0 0 rgba(72, 175, 240, 0), inset 0 0 0 1px rgba(72, 175, 240, 0.4);
            box-shadow:0 0 0 0 rgba(72, 175, 240, 0), 0 0 0 0 rgba(72, 175, 240, 0), inset 0 0 0 1px rgba(72, 175, 240, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-intent-primary.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #48aff0, 0 0 0 3px rgba(72, 175, 240, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px #48aff0, 0 0 0 3px rgba(72, 175, 240, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-intent-success .bp3-editable-text-content{
    color:#3dcc91; }
  .bp3-dark .bp3-editable-text.bp3-intent-success:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(61, 204, 145, 0), 0 0 0 0 rgba(61, 204, 145, 0), inset 0 0 0 1px rgba(61, 204, 145, 0.4);
            box-shadow:0 0 0 0 rgba(61, 204, 145, 0), 0 0 0 0 rgba(61, 204, 145, 0), inset 0 0 0 1px rgba(61, 204, 145, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-intent-success.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #3dcc91, 0 0 0 3px rgba(61, 204, 145, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px #3dcc91, 0 0 0 3px rgba(61, 204, 145, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-intent-warning .bp3-editable-text-content{
    color:#ffb366; }
  .bp3-dark .bp3-editable-text.bp3-intent-warning:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(255, 179, 102, 0), 0 0 0 0 rgba(255, 179, 102, 0), inset 0 0 0 1px rgba(255, 179, 102, 0.4);
            box-shadow:0 0 0 0 rgba(255, 179, 102, 0), 0 0 0 0 rgba(255, 179, 102, 0), inset 0 0 0 1px rgba(255, 179, 102, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-intent-warning.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #ffb366, 0 0 0 3px rgba(255, 179, 102, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px #ffb366, 0 0 0 3px rgba(255, 179, 102, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-intent-danger .bp3-editable-text-content{
    color:#ff7373; }
  .bp3-dark .bp3-editable-text.bp3-intent-danger:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(255, 115, 115, 0), 0 0 0 0 rgba(255, 115, 115, 0), inset 0 0 0 1px rgba(255, 115, 115, 0.4);
            box-shadow:0 0 0 0 rgba(255, 115, 115, 0), 0 0 0 0 rgba(255, 115, 115, 0), inset 0 0 0 1px rgba(255, 115, 115, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-intent-danger.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #ff7373, 0 0 0 3px rgba(255, 115, 115, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px #ff7373, 0 0 0 3px rgba(255, 115, 115, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }

.bp3-editable-text-input,
.bp3-editable-text-content{
  color:inherit;
  display:inherit;
  font:inherit;
  letter-spacing:inherit;
  max-width:inherit;
  min-width:inherit;
  position:relative;
  resize:none;
  text-transform:inherit;
  vertical-align:top; }

.bp3-editable-text-input{
  background:none;
  border:none;
  -webkit-box-shadow:none;
          box-shadow:none;
  padding:0;
  white-space:pre-wrap;
  width:100%; }
  .bp3-editable-text-input::-webkit-input-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-editable-text-input::-moz-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-editable-text-input:-ms-input-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-editable-text-input::-ms-input-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-editable-text-input::placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-editable-text-input:focus{
    outline:none; }
  .bp3-editable-text-input::-ms-clear{
    display:none; }

.bp3-editable-text-content{
  overflow:hidden;
  padding-right:2px;
  text-overflow:ellipsis;
  white-space:pre; }
  .bp3-editable-text-editing > .bp3-editable-text-content{
    left:0;
    position:absolute;
    visibility:hidden; }
  .bp3-editable-text-placeholder > .bp3-editable-text-content{
    color:rgba(92, 112, 128, 0.6); }
    .bp3-dark .bp3-editable-text-placeholder > .bp3-editable-text-content{
      color:rgba(167, 182, 194, 0.6); }

.bp3-editable-text.bp3-multiline{
  display:block; }
  .bp3-editable-text.bp3-multiline .bp3-editable-text-content{
    overflow:auto;
    white-space:pre-wrap;
    word-wrap:break-word; }
.bp3-divider{
  border-bottom:1px solid rgba(16, 22, 26, 0.15);
  border-right:1px solid rgba(16, 22, 26, 0.15);
  margin:5px; }
  .bp3-dark .bp3-divider{
    border-color:rgba(16, 22, 26, 0.4); }
.bp3-control-group{
  -webkit-transform:translateZ(0);
          transform:translateZ(0);
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:normal;
      -ms-flex-direction:row;
          flex-direction:row;
  -webkit-box-align:stretch;
      -ms-flex-align:stretch;
          align-items:stretch; }
  .bp3-control-group > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-control-group > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-control-group .bp3-button,
  .bp3-control-group .bp3-html-select,
  .bp3-control-group .bp3-input,
  .bp3-control-group .bp3-select{
    position:relative; }
  .bp3-control-group .bp3-input{
    border-radius:inherit;
    z-index:2; }
    .bp3-control-group .bp3-input:focus{
      border-radius:3px;
      z-index:14; }
    .bp3-control-group .bp3-input[class*="bp3-intent"]{
      z-index:13; }
      .bp3-control-group .bp3-input[class*="bp3-intent"]:focus{
        z-index:15; }
    .bp3-control-group .bp3-input[readonly], .bp3-control-group .bp3-input:disabled, .bp3-control-group .bp3-input.bp3-disabled{
      z-index:1; }
  .bp3-control-group .bp3-input-group[class*="bp3-intent"] .bp3-input{
    z-index:13; }
    .bp3-control-group .bp3-input-group[class*="bp3-intent"] .bp3-input:focus{
      z-index:15; }
  .bp3-control-group .bp3-button,
  .bp3-control-group .bp3-html-select select,
  .bp3-control-group .bp3-select select{
    -webkit-transform:translateZ(0);
            transform:translateZ(0);
    border-radius:inherit;
    z-index:4; }
    .bp3-control-group .bp3-button:focus,
    .bp3-control-group .bp3-html-select select:focus,
    .bp3-control-group .bp3-select select:focus{
      z-index:5; }
    .bp3-control-group .bp3-button:hover,
    .bp3-control-group .bp3-html-select select:hover,
    .bp3-control-group .bp3-select select:hover{
      z-index:6; }
    .bp3-control-group .bp3-button:active,
    .bp3-control-group .bp3-html-select select:active,
    .bp3-control-group .bp3-select select:active{
      z-index:7; }
    .bp3-control-group .bp3-button[readonly], .bp3-control-group .bp3-button:disabled, .bp3-control-group .bp3-button.bp3-disabled,
    .bp3-control-group .bp3-html-select select[readonly],
    .bp3-control-group .bp3-html-select select:disabled,
    .bp3-control-group .bp3-html-select select.bp3-disabled,
    .bp3-control-group .bp3-select select[readonly],
    .bp3-control-group .bp3-select select:disabled,
    .bp3-control-group .bp3-select select.bp3-disabled{
      z-index:3; }
    .bp3-control-group .bp3-button[class*="bp3-intent"],
    .bp3-control-group .bp3-html-select select[class*="bp3-intent"],
    .bp3-control-group .bp3-select select[class*="bp3-intent"]{
      z-index:9; }
      .bp3-control-group .bp3-button[class*="bp3-intent"]:focus,
      .bp3-control-group .bp3-html-select select[class*="bp3-intent"]:focus,
      .bp3-control-group .bp3-select select[class*="bp3-intent"]:focus{
        z-index:10; }
      .bp3-control-group .bp3-button[class*="bp3-intent"]:hover,
      .bp3-control-group .bp3-html-select select[class*="bp3-intent"]:hover,
      .bp3-control-group .bp3-select select[class*="bp3-intent"]:hover{
        z-index:11; }
      .bp3-control-group .bp3-button[class*="bp3-intent"]:active,
      .bp3-control-group .bp3-html-select select[class*="bp3-intent"]:active,
      .bp3-control-group .bp3-select select[class*="bp3-intent"]:active{
        z-index:12; }
      .bp3-control-group .bp3-button[class*="bp3-intent"][readonly], .bp3-control-group .bp3-button[class*="bp3-intent"]:disabled, .bp3-control-group .bp3-button[class*="bp3-intent"].bp3-disabled,
      .bp3-control-group .bp3-html-select select[class*="bp3-intent"][readonly],
      .bp3-control-group .bp3-html-select select[class*="bp3-intent"]:disabled,
      .bp3-control-group .bp3-html-select select[class*="bp3-intent"].bp3-disabled,
      .bp3-control-group .bp3-select select[class*="bp3-intent"][readonly],
      .bp3-control-group .bp3-select select[class*="bp3-intent"]:disabled,
      .bp3-control-group .bp3-select select[class*="bp3-intent"].bp3-disabled{
        z-index:8; }
  .bp3-control-group .bp3-input-group > .bp3-icon,
  .bp3-control-group .bp3-input-group > .bp3-button,
  .bp3-control-group .bp3-input-group > .bp3-input-left-container,
  .bp3-control-group .bp3-input-group > .bp3-input-action{
    z-index:16; }
  .bp3-control-group .bp3-select::after,
  .bp3-control-group .bp3-html-select::after,
  .bp3-control-group .bp3-select > .bp3-icon,
  .bp3-control-group .bp3-html-select > .bp3-icon{
    z-index:17; }
  .bp3-control-group .bp3-select:focus-within{
    z-index:5; }
  .bp3-control-group:not(.bp3-vertical) > *:not(.bp3-divider){
    margin-right:-1px; }
  .bp3-control-group:not(.bp3-vertical) > .bp3-divider:not(:first-child){
    margin-left:6px; }
  .bp3-dark .bp3-control-group:not(.bp3-vertical) > *:not(.bp3-divider){
    margin-right:0; }
  .bp3-dark .bp3-control-group:not(.bp3-vertical) > .bp3-button + .bp3-button{
    margin-left:1px; }
  .bp3-control-group .bp3-popover-wrapper,
  .bp3-control-group .bp3-popover-target{
    border-radius:inherit; }
  .bp3-control-group > :first-child{
    border-radius:3px 0 0 3px; }
  .bp3-control-group > :last-child{
    border-radius:0 3px 3px 0;
    margin-right:0; }
  .bp3-control-group > :only-child{
    border-radius:3px;
    margin-right:0; }
  .bp3-control-group .bp3-input-group .bp3-button{
    border-radius:3px; }
  .bp3-control-group .bp3-numeric-input:not(:first-child) .bp3-input-group{
    border-bottom-left-radius:0;
    border-top-left-radius:0; }
  .bp3-control-group.bp3-fill{
    width:100%; }
  .bp3-control-group > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto; }
  .bp3-control-group.bp3-fill > *:not(.bp3-fixed){
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto; }
  .bp3-control-group.bp3-vertical{
    -webkit-box-orient:vertical;
    -webkit-box-direction:normal;
        -ms-flex-direction:column;
            flex-direction:column; }
    .bp3-control-group.bp3-vertical > *{
      margin-top:-1px; }
    .bp3-control-group.bp3-vertical > :first-child{
      border-radius:3px 3px 0 0;
      margin-top:0; }
    .bp3-control-group.bp3-vertical > :last-child{
      border-radius:0 0 3px 3px; }
.bp3-control{
  cursor:pointer;
  display:block;
  margin-bottom:10px;
  position:relative;
  text-transform:none; }
  .bp3-control input:checked ~ .bp3-control-indicator{
    background-color:#137cbd;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.1)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.1), rgba(255, 255, 255, 0));
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
    color:#ffffff; }
  .bp3-control:hover input:checked ~ .bp3-control-indicator{
    background-color:#106ba3;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2); }
  .bp3-control input:not(:disabled):active:checked ~ .bp3-control-indicator{
    background:#0e5a8a;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
  .bp3-control input:disabled:checked ~ .bp3-control-indicator{
    background:rgba(19, 124, 189, 0.5);
    -webkit-box-shadow:none;
            box-shadow:none; }
  .bp3-dark .bp3-control input:checked ~ .bp3-control-indicator{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-control:hover input:checked ~ .bp3-control-indicator{
    background-color:#106ba3;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-control input:not(:disabled):active:checked ~ .bp3-control-indicator{
    background-color:#0e5a8a;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
  .bp3-dark .bp3-control input:disabled:checked ~ .bp3-control-indicator{
    background:rgba(14, 90, 138, 0.5);
    -webkit-box-shadow:none;
            box-shadow:none; }
  .bp3-control:not(.bp3-align-right){
    padding-left:26px; }
    .bp3-control:not(.bp3-align-right) .bp3-control-indicator{
      margin-left:-26px; }
  .bp3-control.bp3-align-right{
    padding-right:26px; }
    .bp3-control.bp3-align-right .bp3-control-indicator{
      margin-right:-26px; }
  .bp3-control.bp3-disabled{
    color:rgba(92, 112, 128, 0.6);
    cursor:not-allowed; }
  .bp3-control.bp3-inline{
    display:inline-block;
    margin-right:20px; }
  .bp3-control input{
    left:0;
    opacity:0;
    position:absolute;
    top:0;
    z-index:-1; }
  .bp3-control .bp3-control-indicator{
    background-clip:padding-box;
    background-color:#f5f8fa;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.8)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.8), rgba(255, 255, 255, 0));
    border:none;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
    cursor:pointer;
    display:inline-block;
    font-size:16px;
    height:1em;
    margin-right:10px;
    margin-top:-3px;
    position:relative;
    -webkit-user-select:none;
       -moz-user-select:none;
        -ms-user-select:none;
            user-select:none;
    vertical-align:middle;
    width:1em; }
    .bp3-control .bp3-control-indicator::before{
      content:"";
      display:block;
      height:1em;
      width:1em; }
  .bp3-control:hover .bp3-control-indicator{
    background-color:#ebf1f5; }
  .bp3-control input:not(:disabled):active ~ .bp3-control-indicator{
    background:#d8e1e8;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
  .bp3-control input:disabled ~ .bp3-control-indicator{
    background:rgba(206, 217, 224, 0.5);
    -webkit-box-shadow:none;
            box-shadow:none;
    cursor:not-allowed; }
  .bp3-control input:focus ~ .bp3-control-indicator{
    outline:rgba(19, 124, 189, 0.6) auto 2px;
    outline-offset:2px;
    -moz-outline-radius:6px; }
  .bp3-control.bp3-align-right .bp3-control-indicator{
    float:right;
    margin-left:10px;
    margin-top:1px; }
  .bp3-control.bp3-large{
    font-size:16px; }
    .bp3-control.bp3-large:not(.bp3-align-right){
      padding-left:30px; }
      .bp3-control.bp3-large:not(.bp3-align-right) .bp3-control-indicator{
        margin-left:-30px; }
    .bp3-control.bp3-large.bp3-align-right{
      padding-right:30px; }
      .bp3-control.bp3-large.bp3-align-right .bp3-control-indicator{
        margin-right:-30px; }
    .bp3-control.bp3-large .bp3-control-indicator{
      font-size:20px; }
    .bp3-control.bp3-large.bp3-align-right .bp3-control-indicator{
      margin-top:0; }
  .bp3-control.bp3-checkbox input:indeterminate ~ .bp3-control-indicator{
    background-color:#137cbd;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.1)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.1), rgba(255, 255, 255, 0));
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
    color:#ffffff; }
  .bp3-control.bp3-checkbox:hover input:indeterminate ~ .bp3-control-indicator{
    background-color:#106ba3;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2); }
  .bp3-control.bp3-checkbox input:not(:disabled):active:indeterminate ~ .bp3-control-indicator{
    background:#0e5a8a;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
  .bp3-control.bp3-checkbox input:disabled:indeterminate ~ .bp3-control-indicator{
    background:rgba(19, 124, 189, 0.5);
    -webkit-box-shadow:none;
            box-shadow:none; }
  .bp3-dark .bp3-control.bp3-checkbox input:indeterminate ~ .bp3-control-indicator{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-control.bp3-checkbox:hover input:indeterminate ~ .bp3-control-indicator{
    background-color:#106ba3;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-control.bp3-checkbox input:not(:disabled):active:indeterminate ~ .bp3-control-indicator{
    background-color:#0e5a8a;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
  .bp3-dark .bp3-control.bp3-checkbox input:disabled:indeterminate ~ .bp3-control-indicator{
    background:rgba(14, 90, 138, 0.5);
    -webkit-box-shadow:none;
            box-shadow:none; }
  .bp3-control.bp3-checkbox .bp3-control-indicator{
    border-radius:3px; }
  .bp3-control.bp3-checkbox input:checked ~ .bp3-control-indicator::before{
    background-image:url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 16 16'%3e%3cpath fill-rule='evenodd' clip-rule='evenodd' d='M12 5c-.28 0-.53.11-.71.29L7 9.59l-2.29-2.3a1.003 1.003 0 00-1.42 1.42l3 3c.18.18.43.29.71.29s.53-.11.71-.29l5-5A1.003 1.003 0 0012 5z' fill='white'/%3e%3c/svg%3e"); }
  .bp3-control.bp3-checkbox input:indeterminate ~ .bp3-control-indicator::before{
    background-image:url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 16 16'%3e%3cpath fill-rule='evenodd' clip-rule='evenodd' d='M11 7H5c-.55 0-1 .45-1 1s.45 1 1 1h6c.55 0 1-.45 1-1s-.45-1-1-1z' fill='white'/%3e%3c/svg%3e"); }
  .bp3-control.bp3-radio .bp3-control-indicator{
    border-radius:50%; }
  .bp3-control.bp3-radio input:checked ~ .bp3-control-indicator::before{
    background-image:radial-gradient(#ffffff, #ffffff 28%, transparent 32%); }
  .bp3-control.bp3-radio input:checked:disabled ~ .bp3-control-indicator::before{
    opacity:0.5; }
  .bp3-control.bp3-radio input:focus ~ .bp3-control-indicator{
    -moz-outline-radius:16px; }
  .bp3-control.bp3-switch input ~ .bp3-control-indicator{
    background:rgba(167, 182, 194, 0.5); }
  .bp3-control.bp3-switch:hover input ~ .bp3-control-indicator{
    background:rgba(115, 134, 148, 0.5); }
  .bp3-control.bp3-switch input:not(:disabled):active ~ .bp3-control-indicator{
    background:rgba(92, 112, 128, 0.5); }
  .bp3-control.bp3-switch input:disabled ~ .bp3-control-indicator{
    background:rgba(206, 217, 224, 0.5); }
    .bp3-control.bp3-switch input:disabled ~ .bp3-control-indicator::before{
      background:rgba(255, 255, 255, 0.8); }
  .bp3-control.bp3-switch input:checked ~ .bp3-control-indicator{
    background:#137cbd; }
  .bp3-control.bp3-switch:hover input:checked ~ .bp3-control-indicator{
    background:#106ba3; }
  .bp3-control.bp3-switch input:checked:not(:disabled):active ~ .bp3-control-indicator{
    background:#0e5a8a; }
  .bp3-control.bp3-switch input:checked:disabled ~ .bp3-control-indicator{
    background:rgba(19, 124, 189, 0.5); }
    .bp3-control.bp3-switch input:checked:disabled ~ .bp3-control-indicator::before{
      background:rgba(255, 255, 255, 0.8); }
  .bp3-control.bp3-switch:not(.bp3-align-right){
    padding-left:38px; }
    .bp3-control.bp3-switch:not(.bp3-align-right) .bp3-control-indicator{
      margin-left:-38px; }
  .bp3-control.bp3-switch.bp3-align-right{
    padding-right:38px; }
    .bp3-control.bp3-switch.bp3-align-right .bp3-control-indicator{
      margin-right:-38px; }
  .bp3-control.bp3-switch .bp3-control-indicator{
    border:none;
    border-radius:1.75em;
    -webkit-box-shadow:none !important;
            box-shadow:none !important;
    min-width:1.75em;
    -webkit-transition:background-color 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:background-color 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
    width:auto; }
    .bp3-control.bp3-switch .bp3-control-indicator::before{
      background:#ffffff;
      border-radius:50%;
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.2);
      height:calc(1em - 4px);
      left:0;
      margin:2px;
      position:absolute;
      -webkit-transition:left 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
      transition:left 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
      width:calc(1em - 4px); }
  .bp3-control.bp3-switch input:checked ~ .bp3-control-indicator::before{
    left:calc(100% - 1em); }
  .bp3-control.bp3-switch.bp3-large:not(.bp3-align-right){
    padding-left:45px; }
    .bp3-control.bp3-switch.bp3-large:not(.bp3-align-right) .bp3-control-indicator{
      margin-left:-45px; }
  .bp3-control.bp3-switch.bp3-large.bp3-align-right{
    padding-right:45px; }
    .bp3-control.bp3-switch.bp3-large.bp3-align-right .bp3-control-indicator{
      margin-right:-45px; }
  .bp3-dark .bp3-control.bp3-switch input ~ .bp3-control-indicator{
    background:rgba(16, 22, 26, 0.5); }
  .bp3-dark .bp3-control.bp3-switch:hover input ~ .bp3-control-indicator{
    background:rgba(16, 22, 26, 0.7); }
  .bp3-dark .bp3-control.bp3-switch input:not(:disabled):active ~ .bp3-control-indicator{
    background:rgba(16, 22, 26, 0.9); }
  .bp3-dark .bp3-control.bp3-switch input:disabled ~ .bp3-control-indicator{
    background:rgba(57, 75, 89, 0.5); }
    .bp3-dark .bp3-control.bp3-switch input:disabled ~ .bp3-control-indicator::before{
      background:rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-control.bp3-switch input:checked ~ .bp3-control-indicator{
    background:#137cbd; }
  .bp3-dark .bp3-control.bp3-switch:hover input:checked ~ .bp3-control-indicator{
    background:#106ba3; }
  .bp3-dark .bp3-control.bp3-switch input:checked:not(:disabled):active ~ .bp3-control-indicator{
    background:#0e5a8a; }
  .bp3-dark .bp3-control.bp3-switch input:checked:disabled ~ .bp3-control-indicator{
    background:rgba(14, 90, 138, 0.5); }
    .bp3-dark .bp3-control.bp3-switch input:checked:disabled ~ .bp3-control-indicator::before{
      background:rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-control.bp3-switch .bp3-control-indicator::before{
    background:#394b59;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-control.bp3-switch input:checked ~ .bp3-control-indicator::before{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4); }
  .bp3-control.bp3-switch .bp3-switch-inner-text{
    font-size:0.7em;
    text-align:center; }
  .bp3-control.bp3-switch .bp3-control-indicator-child:first-child{
    line-height:0;
    margin-left:0.5em;
    margin-right:1.2em;
    visibility:hidden; }
  .bp3-control.bp3-switch .bp3-control-indicator-child:last-child{
    line-height:1em;
    margin-left:1.2em;
    margin-right:0.5em;
    visibility:visible; }
  .bp3-control.bp3-switch input:checked ~ .bp3-control-indicator .bp3-control-indicator-child:first-child{
    line-height:1em;
    visibility:visible; }
  .bp3-control.bp3-switch input:checked ~ .bp3-control-indicator .bp3-control-indicator-child:last-child{
    line-height:0;
    visibility:hidden; }
  .bp3-dark .bp3-control{
    color:#f5f8fa; }
    .bp3-dark .bp3-control.bp3-disabled{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-control .bp3-control-indicator{
      background-color:#394b59;
      background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.05)), to(rgba(255, 255, 255, 0)));
      background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.05), rgba(255, 255, 255, 0));
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-control:hover .bp3-control-indicator{
      background-color:#30404d; }
    .bp3-dark .bp3-control input:not(:disabled):active ~ .bp3-control-indicator{
      background:#202b33;
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
    .bp3-dark .bp3-control input:disabled ~ .bp3-control-indicator{
      background:rgba(57, 75, 89, 0.5);
      -webkit-box-shadow:none;
              box-shadow:none;
      cursor:not-allowed; }
    .bp3-dark .bp3-control.bp3-checkbox input:disabled:checked ~ .bp3-control-indicator, .bp3-dark .bp3-control.bp3-checkbox input:disabled:indeterminate ~ .bp3-control-indicator{
      color:rgba(167, 182, 194, 0.6); }
.bp3-file-input{
  cursor:pointer;
  display:inline-block;
  height:30px;
  position:relative; }
  .bp3-file-input input{
    margin:0;
    min-width:200px;
    opacity:0; }
    .bp3-file-input input:disabled + .bp3-file-upload-input,
    .bp3-file-input input.bp3-disabled + .bp3-file-upload-input{
      background:rgba(206, 217, 224, 0.5);
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(92, 112, 128, 0.6);
      cursor:not-allowed;
      resize:none; }
      .bp3-file-input input:disabled + .bp3-file-upload-input::after,
      .bp3-file-input input.bp3-disabled + .bp3-file-upload-input::after{
        background-color:rgba(206, 217, 224, 0.5);
        background-image:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:rgba(92, 112, 128, 0.6);
        cursor:not-allowed;
        outline:none; }
        .bp3-file-input input:disabled + .bp3-file-upload-input::after.bp3-active, .bp3-file-input input:disabled + .bp3-file-upload-input::after.bp3-active:hover,
        .bp3-file-input input.bp3-disabled + .bp3-file-upload-input::after.bp3-active,
        .bp3-file-input input.bp3-disabled + .bp3-file-upload-input::after.bp3-active:hover{
          background:rgba(206, 217, 224, 0.7); }
      .bp3-dark .bp3-file-input input:disabled + .bp3-file-upload-input, .bp3-dark
      .bp3-file-input input.bp3-disabled + .bp3-file-upload-input{
        background:rgba(57, 75, 89, 0.5);
        -webkit-box-shadow:none;
                box-shadow:none;
        color:rgba(167, 182, 194, 0.6); }
        .bp3-dark .bp3-file-input input:disabled + .bp3-file-upload-input::after, .bp3-dark
        .bp3-file-input input.bp3-disabled + .bp3-file-upload-input::after{
          background-color:rgba(57, 75, 89, 0.5);
          background-image:none;
          -webkit-box-shadow:none;
                  box-shadow:none;
          color:rgba(167, 182, 194, 0.6); }
          .bp3-dark .bp3-file-input input:disabled + .bp3-file-upload-input::after.bp3-active, .bp3-dark
          .bp3-file-input input.bp3-disabled + .bp3-file-upload-input::after.bp3-active{
            background:rgba(57, 75, 89, 0.7); }
  .bp3-file-input.bp3-file-input-has-selection .bp3-file-upload-input{
    color:#182026; }
  .bp3-dark .bp3-file-input.bp3-file-input-has-selection .bp3-file-upload-input{
    color:#f5f8fa; }
  .bp3-file-input.bp3-fill{
    width:100%; }
  .bp3-file-input.bp3-large,
  .bp3-large .bp3-file-input{
    height:40px; }
  .bp3-file-input .bp3-file-upload-input-custom-text::after{
    content:attr(bp3-button-text); }

.bp3-file-upload-input{
  -webkit-appearance:none;
     -moz-appearance:none;
          appearance:none;
  background:#ffffff;
  border:none;
  border-radius:3px;
  -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
  color:#182026;
  font-size:14px;
  font-weight:400;
  height:30px;
  line-height:30px;
  outline:none;
  padding:0 10px;
  -webkit-transition:-webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:-webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  vertical-align:middle;
  overflow:hidden;
  text-overflow:ellipsis;
  white-space:nowrap;
  word-wrap:normal;
  color:rgba(92, 112, 128, 0.6);
  left:0;
  padding-right:80px;
  position:absolute;
  right:0;
  top:0;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none; }
  .bp3-file-upload-input::-webkit-input-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-file-upload-input::-moz-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-file-upload-input:-ms-input-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-file-upload-input::-ms-input-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-file-upload-input::placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-file-upload-input:focus, .bp3-file-upload-input.bp3-active{
    -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-file-upload-input[type="search"], .bp3-file-upload-input.bp3-round{
    border-radius:30px;
    -webkit-box-sizing:border-box;
            box-sizing:border-box;
    padding-left:10px; }
  .bp3-file-upload-input[readonly]{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.15);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.15); }
  .bp3-file-upload-input:disabled, .bp3-file-upload-input.bp3-disabled{
    background:rgba(206, 217, 224, 0.5);
    -webkit-box-shadow:none;
            box-shadow:none;
    color:rgba(92, 112, 128, 0.6);
    cursor:not-allowed;
    resize:none; }
  .bp3-file-upload-input::after{
    background-color:#f5f8fa;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.8)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.8), rgba(255, 255, 255, 0));
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
    color:#182026;
    min-height:24px;
    min-width:24px;
    overflow:hidden;
    text-overflow:ellipsis;
    white-space:nowrap;
    word-wrap:normal;
    border-radius:3px;
    content:"Browse";
    line-height:24px;
    margin:3px;
    position:absolute;
    right:0;
    text-align:center;
    top:0;
    width:70px; }
    .bp3-file-upload-input::after:hover{
      background-clip:padding-box;
      background-color:#ebf1f5;
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1); }
    .bp3-file-upload-input::after:active, .bp3-file-upload-input::after.bp3-active{
      background-color:#d8e1e8;
      background-image:none;
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
    .bp3-file-upload-input::after:disabled, .bp3-file-upload-input::after.bp3-disabled{
      background-color:rgba(206, 217, 224, 0.5);
      background-image:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(92, 112, 128, 0.6);
      cursor:not-allowed;
      outline:none; }
      .bp3-file-upload-input::after:disabled.bp3-active, .bp3-file-upload-input::after:disabled.bp3-active:hover, .bp3-file-upload-input::after.bp3-disabled.bp3-active, .bp3-file-upload-input::after.bp3-disabled.bp3-active:hover{
        background:rgba(206, 217, 224, 0.7); }
  .bp3-file-upload-input:hover::after{
    background-clip:padding-box;
    background-color:#ebf1f5;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1); }
  .bp3-file-upload-input:active::after{
    background-color:#d8e1e8;
    background-image:none;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
  .bp3-large .bp3-file-upload-input{
    font-size:16px;
    height:40px;
    line-height:40px;
    padding-right:95px; }
    .bp3-large .bp3-file-upload-input[type="search"], .bp3-large .bp3-file-upload-input.bp3-round{
      padding:0 15px; }
    .bp3-large .bp3-file-upload-input::after{
      min-height:30px;
      min-width:30px;
      line-height:30px;
      margin:5px;
      width:85px; }
  .bp3-dark .bp3-file-upload-input{
    background:rgba(16, 22, 26, 0.3);
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
    color:#f5f8fa;
    color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-file-upload-input::-webkit-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-file-upload-input::-moz-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-file-upload-input:-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-file-upload-input::-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-file-upload-input::placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-file-upload-input:focus{
      -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-file-upload-input[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-file-upload-input:disabled, .bp3-dark .bp3-file-upload-input.bp3-disabled{
      background:rgba(57, 75, 89, 0.5);
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-file-upload-input::after{
      background-color:#394b59;
      background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.05)), to(rgba(255, 255, 255, 0)));
      background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.05), rgba(255, 255, 255, 0));
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
      color:#f5f8fa; }
      .bp3-dark .bp3-file-upload-input::after:hover, .bp3-dark .bp3-file-upload-input::after:active, .bp3-dark .bp3-file-upload-input::after.bp3-active{
        color:#f5f8fa; }
      .bp3-dark .bp3-file-upload-input::after:hover{
        background-color:#30404d;
        -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
                box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-file-upload-input::after:active, .bp3-dark .bp3-file-upload-input::after.bp3-active{
        background-color:#202b33;
        background-image:none;
        -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
                box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
      .bp3-dark .bp3-file-upload-input::after:disabled, .bp3-dark .bp3-file-upload-input::after.bp3-disabled{
        background-color:rgba(57, 75, 89, 0.5);
        background-image:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        color:rgba(167, 182, 194, 0.6); }
        .bp3-dark .bp3-file-upload-input::after:disabled.bp3-active, .bp3-dark .bp3-file-upload-input::after.bp3-disabled.bp3-active{
          background:rgba(57, 75, 89, 0.7); }
      .bp3-dark .bp3-file-upload-input::after .bp3-button-spinner .bp3-spinner-head{
        background:rgba(16, 22, 26, 0.5);
        stroke:#8a9ba8; }
    .bp3-dark .bp3-file-upload-input:hover::after{
      background-color:#30404d;
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-file-upload-input:active::after{
      background-color:#202b33;
      background-image:none;
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
.bp3-file-upload-input::after{
  -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
          box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1); }
.bp3-form-group{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:vertical;
  -webkit-box-direction:normal;
      -ms-flex-direction:column;
          flex-direction:column;
  margin:0 0 15px; }
  .bp3-form-group label.bp3-label{
    margin-bottom:5px; }
  .bp3-form-group .bp3-control{
    margin-top:7px; }
  .bp3-form-group .bp3-form-helper-text{
    color:#5c7080;
    font-size:12px;
    margin-top:5px; }
  .bp3-form-group.bp3-intent-primary .bp3-form-helper-text{
    color:#106ba3; }
  .bp3-form-group.bp3-intent-success .bp3-form-helper-text{
    color:#0d8050; }
  .bp3-form-group.bp3-intent-warning .bp3-form-helper-text{
    color:#bf7326; }
  .bp3-form-group.bp3-intent-danger .bp3-form-helper-text{
    color:#c23030; }
  .bp3-form-group.bp3-inline{
    -webkit-box-align:start;
        -ms-flex-align:start;
            align-items:flex-start;
    -webkit-box-orient:horizontal;
    -webkit-box-direction:normal;
        -ms-flex-direction:row;
            flex-direction:row; }
    .bp3-form-group.bp3-inline.bp3-large label.bp3-label{
      line-height:40px;
      margin:0 10px 0 0; }
    .bp3-form-group.bp3-inline label.bp3-label{
      line-height:30px;
      margin:0 10px 0 0; }
  .bp3-form-group.bp3-disabled .bp3-label,
  .bp3-form-group.bp3-disabled .bp3-text-muted,
  .bp3-form-group.bp3-disabled .bp3-form-helper-text{
    color:rgba(92, 112, 128, 0.6) !important; }
  .bp3-dark .bp3-form-group.bp3-intent-primary .bp3-form-helper-text{
    color:#48aff0; }
  .bp3-dark .bp3-form-group.bp3-intent-success .bp3-form-helper-text{
    color:#3dcc91; }
  .bp3-dark .bp3-form-group.bp3-intent-warning .bp3-form-helper-text{
    color:#ffb366; }
  .bp3-dark .bp3-form-group.bp3-intent-danger .bp3-form-helper-text{
    color:#ff7373; }
  .bp3-dark .bp3-form-group .bp3-form-helper-text{
    color:#a7b6c2; }
  .bp3-dark .bp3-form-group.bp3-disabled .bp3-label,
  .bp3-dark .bp3-form-group.bp3-disabled .bp3-text-muted,
  .bp3-dark .bp3-form-group.bp3-disabled .bp3-form-helper-text{
    color:rgba(167, 182, 194, 0.6) !important; }
.bp3-input-group{
  display:block;
  position:relative; }
  .bp3-input-group .bp3-input{
    position:relative;
    width:100%; }
    .bp3-input-group .bp3-input:not(:first-child){
      padding-left:30px; }
    .bp3-input-group .bp3-input:not(:last-child){
      padding-right:30px; }
  .bp3-input-group .bp3-input-action,
  .bp3-input-group > .bp3-input-left-container,
  .bp3-input-group > .bp3-button,
  .bp3-input-group > .bp3-icon{
    position:absolute;
    top:0; }
    .bp3-input-group .bp3-input-action:first-child,
    .bp3-input-group > .bp3-input-left-container:first-child,
    .bp3-input-group > .bp3-button:first-child,
    .bp3-input-group > .bp3-icon:first-child{
      left:0; }
    .bp3-input-group .bp3-input-action:last-child,
    .bp3-input-group > .bp3-input-left-container:last-child,
    .bp3-input-group > .bp3-button:last-child,
    .bp3-input-group > .bp3-icon:last-child{
      right:0; }
  .bp3-input-group .bp3-button{
    min-height:24px;
    min-width:24px;
    margin:3px;
    padding:0 7px; }
    .bp3-input-group .bp3-button:empty{
      padding:0; }
  .bp3-input-group > .bp3-input-left-container,
  .bp3-input-group > .bp3-icon{
    z-index:1; }
  .bp3-input-group > .bp3-input-left-container > .bp3-icon,
  .bp3-input-group > .bp3-icon{
    color:#5c7080; }
    .bp3-input-group > .bp3-input-left-container > .bp3-icon:empty,
    .bp3-input-group > .bp3-icon:empty{
      font-family:"Icons16", sans-serif;
      font-size:16px;
      font-style:normal;
      font-weight:400;
      line-height:1;
      -moz-osx-font-smoothing:grayscale;
      -webkit-font-smoothing:antialiased; }
  .bp3-input-group > .bp3-input-left-container > .bp3-icon,
  .bp3-input-group > .bp3-icon,
  .bp3-input-group .bp3-input-action > .bp3-spinner{
    margin:7px; }
  .bp3-input-group .bp3-tag{
    margin:5px; }
  .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:not(:hover):not(:focus),
  .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:not(:hover):not(:focus){
    color:#5c7080; }
    .bp3-dark .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:not(:hover):not(:focus), .bp3-dark
    .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:not(:hover):not(:focus){
      color:#a7b6c2; }
    .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:not(:hover):not(:focus) .bp3-icon, .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:not(:hover):not(:focus) .bp3-icon-standard, .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:not(:hover):not(:focus) .bp3-icon-large,
    .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:not(:hover):not(:focus) .bp3-icon,
    .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:not(:hover):not(:focus) .bp3-icon-standard,
    .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:not(:hover):not(:focus) .bp3-icon-large{
      color:#5c7080; }
  .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:disabled,
  .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:disabled{
    color:rgba(92, 112, 128, 0.6) !important; }
    .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:disabled .bp3-icon, .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:disabled .bp3-icon-standard, .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:disabled .bp3-icon-large,
    .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:disabled .bp3-icon,
    .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:disabled .bp3-icon-standard,
    .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:disabled .bp3-icon-large{
      color:rgba(92, 112, 128, 0.6) !important; }
  .bp3-input-group.bp3-disabled{
    cursor:not-allowed; }
    .bp3-input-group.bp3-disabled .bp3-icon{
      color:rgba(92, 112, 128, 0.6); }
  .bp3-input-group.bp3-large .bp3-button{
    min-height:30px;
    min-width:30px;
    margin:5px; }
  .bp3-input-group.bp3-large > .bp3-input-left-container > .bp3-icon,
  .bp3-input-group.bp3-large > .bp3-icon,
  .bp3-input-group.bp3-large .bp3-input-action > .bp3-spinner{
    margin:12px; }
  .bp3-input-group.bp3-large .bp3-input{
    font-size:16px;
    height:40px;
    line-height:40px; }
    .bp3-input-group.bp3-large .bp3-input[type="search"], .bp3-input-group.bp3-large .bp3-input.bp3-round{
      padding:0 15px; }
    .bp3-input-group.bp3-large .bp3-input:not(:first-child){
      padding-left:40px; }
    .bp3-input-group.bp3-large .bp3-input:not(:last-child){
      padding-right:40px; }
  .bp3-input-group.bp3-small .bp3-button{
    min-height:20px;
    min-width:20px;
    margin:2px; }
  .bp3-input-group.bp3-small .bp3-tag{
    min-height:20px;
    min-width:20px;
    margin:2px; }
  .bp3-input-group.bp3-small > .bp3-input-left-container > .bp3-icon,
  .bp3-input-group.bp3-small > .bp3-icon,
  .bp3-input-group.bp3-small .bp3-input-action > .bp3-spinner{
    margin:4px; }
  .bp3-input-group.bp3-small .bp3-input{
    font-size:12px;
    height:24px;
    line-height:24px;
    padding-left:8px;
    padding-right:8px; }
    .bp3-input-group.bp3-small .bp3-input[type="search"], .bp3-input-group.bp3-small .bp3-input.bp3-round{
      padding:0 12px; }
    .bp3-input-group.bp3-small .bp3-input:not(:first-child){
      padding-left:24px; }
    .bp3-input-group.bp3-small .bp3-input:not(:last-child){
      padding-right:24px; }
  .bp3-input-group.bp3-fill{
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto;
    width:100%; }
  .bp3-input-group.bp3-round .bp3-button,
  .bp3-input-group.bp3-round .bp3-input,
  .bp3-input-group.bp3-round .bp3-tag{
    border-radius:30px; }
  .bp3-dark .bp3-input-group .bp3-icon{
    color:#a7b6c2; }
  .bp3-dark .bp3-input-group.bp3-disabled .bp3-icon{
    color:rgba(167, 182, 194, 0.6); }
  .bp3-input-group.bp3-intent-primary .bp3-input{
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px #137cbd, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px #137cbd, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-primary .bp3-input:focus{
      -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-primary .bp3-input[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #137cbd;
              box-shadow:inset 0 0 0 1px #137cbd; }
    .bp3-input-group.bp3-intent-primary .bp3-input:disabled, .bp3-input-group.bp3-intent-primary .bp3-input.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
  .bp3-input-group.bp3-intent-primary > .bp3-icon{
    color:#106ba3; }
    .bp3-dark .bp3-input-group.bp3-intent-primary > .bp3-icon{
      color:#48aff0; }
  .bp3-input-group.bp3-intent-success .bp3-input{
    -webkit-box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px #0f9960, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px #0f9960, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-success .bp3-input:focus{
      -webkit-box-shadow:0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-success .bp3-input[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #0f9960;
              box-shadow:inset 0 0 0 1px #0f9960; }
    .bp3-input-group.bp3-intent-success .bp3-input:disabled, .bp3-input-group.bp3-intent-success .bp3-input.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
  .bp3-input-group.bp3-intent-success > .bp3-icon{
    color:#0d8050; }
    .bp3-dark .bp3-input-group.bp3-intent-success > .bp3-icon{
      color:#3dcc91; }
  .bp3-input-group.bp3-intent-warning .bp3-input{
    -webkit-box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px #d9822b, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px #d9822b, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-warning .bp3-input:focus{
      -webkit-box-shadow:0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-warning .bp3-input[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #d9822b;
              box-shadow:inset 0 0 0 1px #d9822b; }
    .bp3-input-group.bp3-intent-warning .bp3-input:disabled, .bp3-input-group.bp3-intent-warning .bp3-input.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
  .bp3-input-group.bp3-intent-warning > .bp3-icon{
    color:#bf7326; }
    .bp3-dark .bp3-input-group.bp3-intent-warning > .bp3-icon{
      color:#ffb366; }
  .bp3-input-group.bp3-intent-danger .bp3-input{
    -webkit-box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px #db3737, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px #db3737, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-danger .bp3-input:focus{
      -webkit-box-shadow:0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-danger .bp3-input[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #db3737;
              box-shadow:inset 0 0 0 1px #db3737; }
    .bp3-input-group.bp3-intent-danger .bp3-input:disabled, .bp3-input-group.bp3-intent-danger .bp3-input.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
  .bp3-input-group.bp3-intent-danger > .bp3-icon{
    color:#c23030; }
    .bp3-dark .bp3-input-group.bp3-intent-danger > .bp3-icon{
      color:#ff7373; }
.bp3-input{
  -webkit-appearance:none;
     -moz-appearance:none;
          appearance:none;
  background:#ffffff;
  border:none;
  border-radius:3px;
  -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
  color:#182026;
  font-size:14px;
  font-weight:400;
  height:30px;
  line-height:30px;
  outline:none;
  padding:0 10px;
  -webkit-transition:-webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:-webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  vertical-align:middle; }
  .bp3-input::-webkit-input-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-input::-moz-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-input:-ms-input-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-input::-ms-input-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-input::placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-input:focus, .bp3-input.bp3-active{
    -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-input[type="search"], .bp3-input.bp3-round{
    border-radius:30px;
    -webkit-box-sizing:border-box;
            box-sizing:border-box;
    padding-left:10px; }
  .bp3-input[readonly]{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.15);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.15); }
  .bp3-input:disabled, .bp3-input.bp3-disabled{
    background:rgba(206, 217, 224, 0.5);
    -webkit-box-shadow:none;
            box-shadow:none;
    color:rgba(92, 112, 128, 0.6);
    cursor:not-allowed;
    resize:none; }
  .bp3-input.bp3-large{
    font-size:16px;
    height:40px;
    line-height:40px; }
    .bp3-input.bp3-large[type="search"], .bp3-input.bp3-large.bp3-round{
      padding:0 15px; }
  .bp3-input.bp3-small{
    font-size:12px;
    height:24px;
    line-height:24px;
    padding-left:8px;
    padding-right:8px; }
    .bp3-input.bp3-small[type="search"], .bp3-input.bp3-small.bp3-round{
      padding:0 12px; }
  .bp3-input.bp3-fill{
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto;
    width:100%; }
  .bp3-dark .bp3-input{
    background:rgba(16, 22, 26, 0.3);
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
    color:#f5f8fa; }
    .bp3-dark .bp3-input::-webkit-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-input::-moz-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-input:-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-input::-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-input::placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-input:focus{
      -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-input[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-input:disabled, .bp3-dark .bp3-input.bp3-disabled{
      background:rgba(57, 75, 89, 0.5);
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(167, 182, 194, 0.6); }
  .bp3-input.bp3-intent-primary{
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px #137cbd, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px #137cbd, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-primary:focus{
      -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-primary[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #137cbd;
              box-shadow:inset 0 0 0 1px #137cbd; }
    .bp3-input.bp3-intent-primary:disabled, .bp3-input.bp3-intent-primary.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
    .bp3-dark .bp3-input.bp3-intent-primary{
      -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px #137cbd, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px #137cbd, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-primary:focus{
        -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
                box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-primary[readonly]{
        -webkit-box-shadow:inset 0 0 0 1px #137cbd;
                box-shadow:inset 0 0 0 1px #137cbd; }
      .bp3-dark .bp3-input.bp3-intent-primary:disabled, .bp3-dark .bp3-input.bp3-intent-primary.bp3-disabled{
        -webkit-box-shadow:none;
                box-shadow:none; }
  .bp3-input.bp3-intent-success{
    -webkit-box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px #0f9960, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px #0f9960, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-success:focus{
      -webkit-box-shadow:0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-success[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #0f9960;
              box-shadow:inset 0 0 0 1px #0f9960; }
    .bp3-input.bp3-intent-success:disabled, .bp3-input.bp3-intent-success.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
    .bp3-dark .bp3-input.bp3-intent-success{
      -webkit-box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px #0f9960, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px #0f9960, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-success:focus{
        -webkit-box-shadow:0 0 0 1px #0f9960, 0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
                box-shadow:0 0 0 1px #0f9960, 0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-success[readonly]{
        -webkit-box-shadow:inset 0 0 0 1px #0f9960;
                box-shadow:inset 0 0 0 1px #0f9960; }
      .bp3-dark .bp3-input.bp3-intent-success:disabled, .bp3-dark .bp3-input.bp3-intent-success.bp3-disabled{
        -webkit-box-shadow:none;
                box-shadow:none; }
  .bp3-input.bp3-intent-warning{
    -webkit-box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px #d9822b, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px #d9822b, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-warning:focus{
      -webkit-box-shadow:0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-warning[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #d9822b;
              box-shadow:inset 0 0 0 1px #d9822b; }
    .bp3-input.bp3-intent-warning:disabled, .bp3-input.bp3-intent-warning.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
    .bp3-dark .bp3-input.bp3-intent-warning{
      -webkit-box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px #d9822b, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px #d9822b, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-warning:focus{
        -webkit-box-shadow:0 0 0 1px #d9822b, 0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
                box-shadow:0 0 0 1px #d9822b, 0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-warning[readonly]{
        -webkit-box-shadow:inset 0 0 0 1px #d9822b;
                box-shadow:inset 0 0 0 1px #d9822b; }
      .bp3-dark .bp3-input.bp3-intent-warning:disabled, .bp3-dark .bp3-input.bp3-intent-warning.bp3-disabled{
        -webkit-box-shadow:none;
                box-shadow:none; }
  .bp3-input.bp3-intent-danger{
    -webkit-box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px #db3737, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px #db3737, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-danger:focus{
      -webkit-box-shadow:0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-danger[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #db3737;
              box-shadow:inset 0 0 0 1px #db3737; }
    .bp3-input.bp3-intent-danger:disabled, .bp3-input.bp3-intent-danger.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
    .bp3-dark .bp3-input.bp3-intent-danger{
      -webkit-box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px #db3737, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px #db3737, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-danger:focus{
        -webkit-box-shadow:0 0 0 1px #db3737, 0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
                box-shadow:0 0 0 1px #db3737, 0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-danger[readonly]{
        -webkit-box-shadow:inset 0 0 0 1px #db3737;
                box-shadow:inset 0 0 0 1px #db3737; }
      .bp3-dark .bp3-input.bp3-intent-danger:disabled, .bp3-dark .bp3-input.bp3-intent-danger.bp3-disabled{
        -webkit-box-shadow:none;
                box-shadow:none; }
  .bp3-input::-ms-clear{
    display:none; }
textarea.bp3-input{
  max-width:100%;
  padding:10px; }
  textarea.bp3-input, textarea.bp3-input.bp3-large, textarea.bp3-input.bp3-small{
    height:auto;
    line-height:inherit; }
  textarea.bp3-input.bp3-small{
    padding:8px; }
  .bp3-dark textarea.bp3-input{
    background:rgba(16, 22, 26, 0.3);
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
    color:#f5f8fa; }
    .bp3-dark textarea.bp3-input::-webkit-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark textarea.bp3-input::-moz-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark textarea.bp3-input:-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark textarea.bp3-input::-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark textarea.bp3-input::placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark textarea.bp3-input:focus{
      -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark textarea.bp3-input[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark textarea.bp3-input:disabled, .bp3-dark textarea.bp3-input.bp3-disabled{
      background:rgba(57, 75, 89, 0.5);
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(167, 182, 194, 0.6); }
label.bp3-label{
  display:block;
  margin-bottom:15px;
  margin-top:0; }
  label.bp3-label .bp3-html-select,
  label.bp3-label .bp3-input,
  label.bp3-label .bp3-select,
  label.bp3-label .bp3-slider,
  label.bp3-label .bp3-popover-wrapper{
    display:block;
    margin-top:5px;
    text-transform:none; }
  label.bp3-label .bp3-button-group{
    margin-top:5px; }
  label.bp3-label .bp3-select select,
  label.bp3-label .bp3-html-select select{
    font-weight:400;
    vertical-align:top;
    width:100%; }
  label.bp3-label.bp3-disabled,
  label.bp3-label.bp3-disabled .bp3-text-muted{
    color:rgba(92, 112, 128, 0.6); }
  label.bp3-label.bp3-inline{
    line-height:30px; }
    label.bp3-label.bp3-inline .bp3-html-select,
    label.bp3-label.bp3-inline .bp3-input,
    label.bp3-label.bp3-inline .bp3-input-group,
    label.bp3-label.bp3-inline .bp3-select,
    label.bp3-label.bp3-inline .bp3-popover-wrapper{
      display:inline-block;
      margin:0 0 0 5px;
      vertical-align:top; }
    label.bp3-label.bp3-inline .bp3-button-group{
      margin:0 0 0 5px; }
    label.bp3-label.bp3-inline .bp3-input-group .bp3-input{
      margin-left:0; }
    label.bp3-label.bp3-inline.bp3-large{
      line-height:40px; }
  label.bp3-label:not(.bp3-inline) .bp3-popover-target{
    display:block; }
  .bp3-dark label.bp3-label{
    color:#f5f8fa; }
    .bp3-dark label.bp3-label.bp3-disabled,
    .bp3-dark label.bp3-label.bp3-disabled .bp3-text-muted{
      color:rgba(167, 182, 194, 0.6); }
.bp3-numeric-input .bp3-button-group.bp3-vertical > .bp3-button{
  -webkit-box-flex:1;
      -ms-flex:1 1 14px;
          flex:1 1 14px;
  min-height:0;
  padding:0;
  width:30px; }
  .bp3-numeric-input .bp3-button-group.bp3-vertical > .bp3-button:first-child{
    border-radius:0 3px 0 0; }
  .bp3-numeric-input .bp3-button-group.bp3-vertical > .bp3-button:last-child{
    border-radius:0 0 3px 0; }

.bp3-numeric-input .bp3-button-group.bp3-vertical:first-child > .bp3-button:first-child{
  border-radius:3px 0 0 0; }

.bp3-numeric-input .bp3-button-group.bp3-vertical:first-child > .bp3-button:last-child{
  border-radius:0 0 0 3px; }

.bp3-numeric-input.bp3-large .bp3-button-group.bp3-vertical > .bp3-button{
  width:40px; }

form{
  display:block; }
.bp3-html-select select,
.bp3-select select{
  display:-webkit-inline-box;
  display:-ms-inline-flexbox;
  display:inline-flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:normal;
      -ms-flex-direction:row;
          flex-direction:row;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  border:none;
  border-radius:3px;
  cursor:pointer;
  font-size:14px;
  -webkit-box-pack:center;
      -ms-flex-pack:center;
          justify-content:center;
  padding:5px 10px;
  text-align:left;
  vertical-align:middle;
  background-color:#f5f8fa;
  background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.8)), to(rgba(255, 255, 255, 0)));
  background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.8), rgba(255, 255, 255, 0));
  -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
          box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
  color:#182026;
  -moz-appearance:none;
  -webkit-appearance:none;
  border-radius:3px;
  height:30px;
  padding:0 25px 0 10px;
  width:100%; }
  .bp3-html-select select > *, .bp3-select select > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-html-select select > .bp3-fill, .bp3-select select > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-html-select select::before,
  .bp3-select select::before, .bp3-html-select select > *, .bp3-select select > *{
    margin-right:7px; }
  .bp3-html-select select:empty::before,
  .bp3-select select:empty::before,
  .bp3-html-select select > :last-child,
  .bp3-select select > :last-child{
    margin-right:0; }
  .bp3-html-select select:hover,
  .bp3-select select:hover{
    background-clip:padding-box;
    background-color:#ebf1f5;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1); }
  .bp3-html-select select:active,
  .bp3-select select:active, .bp3-html-select select.bp3-active,
  .bp3-select select.bp3-active{
    background-color:#d8e1e8;
    background-image:none;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
  .bp3-html-select select:disabled,
  .bp3-select select:disabled, .bp3-html-select select.bp3-disabled,
  .bp3-select select.bp3-disabled{
    background-color:rgba(206, 217, 224, 0.5);
    background-image:none;
    -webkit-box-shadow:none;
            box-shadow:none;
    color:rgba(92, 112, 128, 0.6);
    cursor:not-allowed;
    outline:none; }
    .bp3-html-select select:disabled.bp3-active,
    .bp3-select select:disabled.bp3-active, .bp3-html-select select:disabled.bp3-active:hover,
    .bp3-select select:disabled.bp3-active:hover, .bp3-html-select select.bp3-disabled.bp3-active,
    .bp3-select select.bp3-disabled.bp3-active, .bp3-html-select select.bp3-disabled.bp3-active:hover,
    .bp3-select select.bp3-disabled.bp3-active:hover{
      background:rgba(206, 217, 224, 0.7); }

.bp3-html-select.bp3-minimal select,
.bp3-select.bp3-minimal select{
  background:none;
  -webkit-box-shadow:none;
          box-shadow:none; }
  .bp3-html-select.bp3-minimal select:hover,
  .bp3-select.bp3-minimal select:hover{
    background:rgba(167, 182, 194, 0.3);
    -webkit-box-shadow:none;
            box-shadow:none;
    color:#182026;
    text-decoration:none; }
  .bp3-html-select.bp3-minimal select:active,
  .bp3-select.bp3-minimal select:active, .bp3-html-select.bp3-minimal select.bp3-active,
  .bp3-select.bp3-minimal select.bp3-active{
    background:rgba(115, 134, 148, 0.3);
    -webkit-box-shadow:none;
            box-shadow:none;
    color:#182026; }
  .bp3-html-select.bp3-minimal select:disabled,
  .bp3-select.bp3-minimal select:disabled, .bp3-html-select.bp3-minimal select:disabled:hover,
  .bp3-select.bp3-minimal select:disabled:hover, .bp3-html-select.bp3-minimal select.bp3-disabled,
  .bp3-select.bp3-minimal select.bp3-disabled, .bp3-html-select.bp3-minimal select.bp3-disabled:hover,
  .bp3-select.bp3-minimal select.bp3-disabled:hover{
    background:none;
    color:rgba(92, 112, 128, 0.6);
    cursor:not-allowed; }
    .bp3-html-select.bp3-minimal select:disabled.bp3-active,
    .bp3-select.bp3-minimal select:disabled.bp3-active, .bp3-html-select.bp3-minimal select:disabled:hover.bp3-active,
    .bp3-select.bp3-minimal select:disabled:hover.bp3-active, .bp3-html-select.bp3-minimal select.bp3-disabled.bp3-active,
    .bp3-select.bp3-minimal select.bp3-disabled.bp3-active, .bp3-html-select.bp3-minimal select.bp3-disabled:hover.bp3-active,
    .bp3-select.bp3-minimal select.bp3-disabled:hover.bp3-active{
      background:rgba(115, 134, 148, 0.3); }
  .bp3-dark .bp3-html-select.bp3-minimal select, .bp3-html-select.bp3-minimal .bp3-dark select,
  .bp3-dark .bp3-select.bp3-minimal select, .bp3-select.bp3-minimal .bp3-dark select{
    background:none;
    -webkit-box-shadow:none;
            box-shadow:none;
    color:inherit; }
    .bp3-dark .bp3-html-select.bp3-minimal select:hover, .bp3-html-select.bp3-minimal .bp3-dark select:hover,
    .bp3-dark .bp3-select.bp3-minimal select:hover, .bp3-select.bp3-minimal .bp3-dark select:hover, .bp3-dark .bp3-html-select.bp3-minimal select:active, .bp3-html-select.bp3-minimal .bp3-dark select:active,
    .bp3-dark .bp3-select.bp3-minimal select:active, .bp3-select.bp3-minimal .bp3-dark select:active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-active,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-active{
      background:none;
      -webkit-box-shadow:none;
              box-shadow:none; }
    .bp3-dark .bp3-html-select.bp3-minimal select:hover, .bp3-html-select.bp3-minimal .bp3-dark select:hover,
    .bp3-dark .bp3-select.bp3-minimal select:hover, .bp3-select.bp3-minimal .bp3-dark select:hover{
      background:rgba(138, 155, 168, 0.15); }
    .bp3-dark .bp3-html-select.bp3-minimal select:active, .bp3-html-select.bp3-minimal .bp3-dark select:active,
    .bp3-dark .bp3-select.bp3-minimal select:active, .bp3-select.bp3-minimal .bp3-dark select:active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-active,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-active{
      background:rgba(138, 155, 168, 0.3);
      color:#f5f8fa; }
    .bp3-dark .bp3-html-select.bp3-minimal select:disabled, .bp3-html-select.bp3-minimal .bp3-dark select:disabled,
    .bp3-dark .bp3-select.bp3-minimal select:disabled, .bp3-select.bp3-minimal .bp3-dark select:disabled, .bp3-dark .bp3-html-select.bp3-minimal select:disabled:hover, .bp3-html-select.bp3-minimal .bp3-dark select:disabled:hover,
    .bp3-dark .bp3-select.bp3-minimal select:disabled:hover, .bp3-select.bp3-minimal .bp3-dark select:disabled:hover, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-disabled,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-disabled, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-disabled:hover, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-disabled:hover,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-disabled:hover, .bp3-select.bp3-minimal .bp3-dark select.bp3-disabled:hover{
      background:none;
      color:rgba(167, 182, 194, 0.6);
      cursor:not-allowed; }
      .bp3-dark .bp3-html-select.bp3-minimal select:disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select:disabled.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select:disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select:disabled.bp3-active, .bp3-dark .bp3-html-select.bp3-minimal select:disabled:hover.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select:disabled:hover.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select:disabled:hover.bp3-active, .bp3-select.bp3-minimal .bp3-dark select:disabled:hover.bp3-active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-disabled.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-disabled.bp3-active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-disabled:hover.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-disabled:hover.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-disabled:hover.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-disabled:hover.bp3-active{
        background:rgba(138, 155, 168, 0.3); }
  .bp3-html-select.bp3-minimal select.bp3-intent-primary,
  .bp3-select.bp3-minimal select.bp3-intent-primary{
    color:#106ba3; }
    .bp3-html-select.bp3-minimal select.bp3-intent-primary:hover,
    .bp3-select.bp3-minimal select.bp3-intent-primary:hover, .bp3-html-select.bp3-minimal select.bp3-intent-primary:active,
    .bp3-select.bp3-minimal select.bp3-intent-primary:active, .bp3-html-select.bp3-minimal select.bp3-intent-primary.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-primary.bp3-active{
      background:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:#106ba3; }
    .bp3-html-select.bp3-minimal select.bp3-intent-primary:hover,
    .bp3-select.bp3-minimal select.bp3-intent-primary:hover{
      background:rgba(19, 124, 189, 0.15);
      color:#106ba3; }
    .bp3-html-select.bp3-minimal select.bp3-intent-primary:active,
    .bp3-select.bp3-minimal select.bp3-intent-primary:active, .bp3-html-select.bp3-minimal select.bp3-intent-primary.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-primary.bp3-active{
      background:rgba(19, 124, 189, 0.3);
      color:#106ba3; }
    .bp3-html-select.bp3-minimal select.bp3-intent-primary:disabled,
    .bp3-select.bp3-minimal select.bp3-intent-primary:disabled, .bp3-html-select.bp3-minimal select.bp3-intent-primary.bp3-disabled,
    .bp3-select.bp3-minimal select.bp3-intent-primary.bp3-disabled{
      background:none;
      color:rgba(16, 107, 163, 0.5); }
      .bp3-html-select.bp3-minimal select.bp3-intent-primary:disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-primary:disabled.bp3-active, .bp3-html-select.bp3-minimal select.bp3-intent-primary.bp3-disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-primary.bp3-disabled.bp3-active{
        background:rgba(19, 124, 189, 0.3); }
    .bp3-html-select.bp3-minimal select.bp3-intent-primary .bp3-button-spinner .bp3-spinner-head, .bp3-select.bp3-minimal select.bp3-intent-primary .bp3-button-spinner .bp3-spinner-head{
      stroke:#106ba3; }
    .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary{
      color:#48aff0; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary:hover, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary:hover,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary:hover, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary:hover{
        background:rgba(19, 124, 189, 0.2);
        color:#48aff0; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary:active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary:active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary:active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary:active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary.bp3-active{
        background:rgba(19, 124, 189, 0.3);
        color:#48aff0; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary:disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary:disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary:disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary:disabled, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary.bp3-disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary.bp3-disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary.bp3-disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary.bp3-disabled{
        background:none;
        color:rgba(72, 175, 240, 0.5); }
        .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary:disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary:disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary:disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary:disabled.bp3-active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary.bp3-disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary.bp3-disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary.bp3-disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary.bp3-disabled.bp3-active{
          background:rgba(19, 124, 189, 0.3); }
  .bp3-html-select.bp3-minimal select.bp3-intent-success,
  .bp3-select.bp3-minimal select.bp3-intent-success{
    color:#0d8050; }
    .bp3-html-select.bp3-minimal select.bp3-intent-success:hover,
    .bp3-select.bp3-minimal select.bp3-intent-success:hover, .bp3-html-select.bp3-minimal select.bp3-intent-success:active,
    .bp3-select.bp3-minimal select.bp3-intent-success:active, .bp3-html-select.bp3-minimal select.bp3-intent-success.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-success.bp3-active{
      background:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:#0d8050; }
    .bp3-html-select.bp3-minimal select.bp3-intent-success:hover,
    .bp3-select.bp3-minimal select.bp3-intent-success:hover{
      background:rgba(15, 153, 96, 0.15);
      color:#0d8050; }
    .bp3-html-select.bp3-minimal select.bp3-intent-success:active,
    .bp3-select.bp3-minimal select.bp3-intent-success:active, .bp3-html-select.bp3-minimal select.bp3-intent-success.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-success.bp3-active{
      background:rgba(15, 153, 96, 0.3);
      color:#0d8050; }
    .bp3-html-select.bp3-minimal select.bp3-intent-success:disabled,
    .bp3-select.bp3-minimal select.bp3-intent-success:disabled, .bp3-html-select.bp3-minimal select.bp3-intent-success.bp3-disabled,
    .bp3-select.bp3-minimal select.bp3-intent-success.bp3-disabled{
      background:none;
      color:rgba(13, 128, 80, 0.5); }
      .bp3-html-select.bp3-minimal select.bp3-intent-success:disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-success:disabled.bp3-active, .bp3-html-select.bp3-minimal select.bp3-intent-success.bp3-disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-success.bp3-disabled.bp3-active{
        background:rgba(15, 153, 96, 0.3); }
    .bp3-html-select.bp3-minimal select.bp3-intent-success .bp3-button-spinner .bp3-spinner-head, .bp3-select.bp3-minimal select.bp3-intent-success .bp3-button-spinner .bp3-spinner-head{
      stroke:#0d8050; }
    .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success{
      color:#3dcc91; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success:hover, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success:hover,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success:hover, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success:hover{
        background:rgba(15, 153, 96, 0.2);
        color:#3dcc91; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success:active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success:active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success:active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success:active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success.bp3-active{
        background:rgba(15, 153, 96, 0.3);
        color:#3dcc91; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success:disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success:disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success:disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success:disabled, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success.bp3-disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success.bp3-disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success.bp3-disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success.bp3-disabled{
        background:none;
        color:rgba(61, 204, 145, 0.5); }
        .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success:disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success:disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success:disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success:disabled.bp3-active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success.bp3-disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success.bp3-disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success.bp3-disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success.bp3-disabled.bp3-active{
          background:rgba(15, 153, 96, 0.3); }
  .bp3-html-select.bp3-minimal select.bp3-intent-warning,
  .bp3-select.bp3-minimal select.bp3-intent-warning{
    color:#bf7326; }
    .bp3-html-select.bp3-minimal select.bp3-intent-warning:hover,
    .bp3-select.bp3-minimal select.bp3-intent-warning:hover, .bp3-html-select.bp3-minimal select.bp3-intent-warning:active,
    .bp3-select.bp3-minimal select.bp3-intent-warning:active, .bp3-html-select.bp3-minimal select.bp3-intent-warning.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-warning.bp3-active{
      background:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:#bf7326; }
    .bp3-html-select.bp3-minimal select.bp3-intent-warning:hover,
    .bp3-select.bp3-minimal select.bp3-intent-warning:hover{
      background:rgba(217, 130, 43, 0.15);
      color:#bf7326; }
    .bp3-html-select.bp3-minimal select.bp3-intent-warning:active,
    .bp3-select.bp3-minimal select.bp3-intent-warning:active, .bp3-html-select.bp3-minimal select.bp3-intent-warning.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-warning.bp3-active{
      background:rgba(217, 130, 43, 0.3);
      color:#bf7326; }
    .bp3-html-select.bp3-minimal select.bp3-intent-warning:disabled,
    .bp3-select.bp3-minimal select.bp3-intent-warning:disabled, .bp3-html-select.bp3-minimal select.bp3-intent-warning.bp3-disabled,
    .bp3-select.bp3-minimal select.bp3-intent-warning.bp3-disabled{
      background:none;
      color:rgba(191, 115, 38, 0.5); }
      .bp3-html-select.bp3-minimal select.bp3-intent-warning:disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-warning:disabled.bp3-active, .bp3-html-select.bp3-minimal select.bp3-intent-warning.bp3-disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-warning.bp3-disabled.bp3-active{
        background:rgba(217, 130, 43, 0.3); }
    .bp3-html-select.bp3-minimal select.bp3-intent-warning .bp3-button-spinner .bp3-spinner-head, .bp3-select.bp3-minimal select.bp3-intent-warning .bp3-button-spinner .bp3-spinner-head{
      stroke:#bf7326; }
    .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning{
      color:#ffb366; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning:hover, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning:hover,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning:hover, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning:hover{
        background:rgba(217, 130, 43, 0.2);
        color:#ffb366; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning:active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning:active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning:active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning:active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning.bp3-active{
        background:rgba(217, 130, 43, 0.3);
        color:#ffb366; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning:disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning:disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning:disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning:disabled, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning.bp3-disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning.bp3-disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning.bp3-disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning.bp3-disabled{
        background:none;
        color:rgba(255, 179, 102, 0.5); }
        .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning:disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning:disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning:disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning:disabled.bp3-active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning.bp3-disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning.bp3-disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning.bp3-disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning.bp3-disabled.bp3-active{
          background:rgba(217, 130, 43, 0.3); }
  .bp3-html-select.bp3-minimal select.bp3-intent-danger,
  .bp3-select.bp3-minimal select.bp3-intent-danger{
    color:#c23030; }
    .bp3-html-select.bp3-minimal select.bp3-intent-danger:hover,
    .bp3-select.bp3-minimal select.bp3-intent-danger:hover, .bp3-html-select.bp3-minimal select.bp3-intent-danger:active,
    .bp3-select.bp3-minimal select.bp3-intent-danger:active, .bp3-html-select.bp3-minimal select.bp3-intent-danger.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-danger.bp3-active{
      background:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:#c23030; }
    .bp3-html-select.bp3-minimal select.bp3-intent-danger:hover,
    .bp3-select.bp3-minimal select.bp3-intent-danger:hover{
      background:rgba(219, 55, 55, 0.15);
      color:#c23030; }
    .bp3-html-select.bp3-minimal select.bp3-intent-danger:active,
    .bp3-select.bp3-minimal select.bp3-intent-danger:active, .bp3-html-select.bp3-minimal select.bp3-intent-danger.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-danger.bp3-active{
      background:rgba(219, 55, 55, 0.3);
      color:#c23030; }
    .bp3-html-select.bp3-minimal select.bp3-intent-danger:disabled,
    .bp3-select.bp3-minimal select.bp3-intent-danger:disabled, .bp3-html-select.bp3-minimal select.bp3-intent-danger.bp3-disabled,
    .bp3-select.bp3-minimal select.bp3-intent-danger.bp3-disabled{
      background:none;
      color:rgba(194, 48, 48, 0.5); }
      .bp3-html-select.bp3-minimal select.bp3-intent-danger:disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-danger:disabled.bp3-active, .bp3-html-select.bp3-minimal select.bp3-intent-danger.bp3-disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-danger.bp3-disabled.bp3-active{
        background:rgba(219, 55, 55, 0.3); }
    .bp3-html-select.bp3-minimal select.bp3-intent-danger .bp3-button-spinner .bp3-spinner-head, .bp3-select.bp3-minimal select.bp3-intent-danger .bp3-button-spinner .bp3-spinner-head{
      stroke:#c23030; }
    .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger{
      color:#ff7373; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger:hover, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger:hover,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger:hover, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger:hover{
        background:rgba(219, 55, 55, 0.2);
        color:#ff7373; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger:active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger:active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger:active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger:active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger.bp3-active{
        background:rgba(219, 55, 55, 0.3);
        color:#ff7373; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger:disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger:disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger:disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger:disabled, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger.bp3-disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger.bp3-disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger.bp3-disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger.bp3-disabled{
        background:none;
        color:rgba(255, 115, 115, 0.5); }
        .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger:disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger:disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger:disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger:disabled.bp3-active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger.bp3-disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger.bp3-disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger.bp3-disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger.bp3-disabled.bp3-active{
          background:rgba(219, 55, 55, 0.3); }

.bp3-html-select.bp3-large select,
.bp3-select.bp3-large select{
  font-size:16px;
  height:40px;
  padding-right:35px; }

.bp3-dark .bp3-html-select select, .bp3-dark .bp3-select select{
  background-color:#394b59;
  background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.05)), to(rgba(255, 255, 255, 0)));
  background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.05), rgba(255, 255, 255, 0));
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
  color:#f5f8fa; }
  .bp3-dark .bp3-html-select select:hover, .bp3-dark .bp3-select select:hover, .bp3-dark .bp3-html-select select:active, .bp3-dark .bp3-select select:active, .bp3-dark .bp3-html-select select.bp3-active, .bp3-dark .bp3-select select.bp3-active{
    color:#f5f8fa; }
  .bp3-dark .bp3-html-select select:hover, .bp3-dark .bp3-select select:hover{
    background-color:#30404d;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-html-select select:active, .bp3-dark .bp3-select select:active, .bp3-dark .bp3-html-select select.bp3-active, .bp3-dark .bp3-select select.bp3-active{
    background-color:#202b33;
    background-image:none;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
  .bp3-dark .bp3-html-select select:disabled, .bp3-dark .bp3-select select:disabled, .bp3-dark .bp3-html-select select.bp3-disabled, .bp3-dark .bp3-select select.bp3-disabled{
    background-color:rgba(57, 75, 89, 0.5);
    background-image:none;
    -webkit-box-shadow:none;
            box-shadow:none;
    color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-html-select select:disabled.bp3-active, .bp3-dark .bp3-select select:disabled.bp3-active, .bp3-dark .bp3-html-select select.bp3-disabled.bp3-active, .bp3-dark .bp3-select select.bp3-disabled.bp3-active{
      background:rgba(57, 75, 89, 0.7); }
  .bp3-dark .bp3-html-select select .bp3-button-spinner .bp3-spinner-head, .bp3-dark .bp3-select select .bp3-button-spinner .bp3-spinner-head{
    background:rgba(16, 22, 26, 0.5);
    stroke:#8a9ba8; }

.bp3-html-select select:disabled,
.bp3-select select:disabled{
  background-color:rgba(206, 217, 224, 0.5);
  -webkit-box-shadow:none;
          box-shadow:none;
  color:rgba(92, 112, 128, 0.6);
  cursor:not-allowed; }

.bp3-html-select .bp3-icon,
.bp3-select .bp3-icon, .bp3-select::after{
  color:#5c7080;
  pointer-events:none;
  position:absolute;
  right:7px;
  top:7px; }
  .bp3-html-select .bp3-disabled.bp3-icon,
  .bp3-select .bp3-disabled.bp3-icon, .bp3-disabled.bp3-select::after{
    color:rgba(92, 112, 128, 0.6); }
.bp3-html-select,
.bp3-select{
  display:inline-block;
  letter-spacing:normal;
  position:relative;
  vertical-align:middle; }
  .bp3-html-select select::-ms-expand,
  .bp3-select select::-ms-expand{
    display:none; }
  .bp3-html-select .bp3-icon,
  .bp3-select .bp3-icon{
    color:#5c7080; }
    .bp3-html-select .bp3-icon:hover,
    .bp3-select .bp3-icon:hover{
      color:#182026; }
    .bp3-dark .bp3-html-select .bp3-icon, .bp3-dark
    .bp3-select .bp3-icon{
      color:#a7b6c2; }
      .bp3-dark .bp3-html-select .bp3-icon:hover, .bp3-dark
      .bp3-select .bp3-icon:hover{
        color:#f5f8fa; }
  .bp3-html-select.bp3-large::after,
  .bp3-html-select.bp3-large .bp3-icon,
  .bp3-select.bp3-large::after,
  .bp3-select.bp3-large .bp3-icon{
    right:12px;
    top:12px; }
  .bp3-html-select.bp3-fill,
  .bp3-html-select.bp3-fill select,
  .bp3-select.bp3-fill,
  .bp3-select.bp3-fill select{
    width:100%; }
  .bp3-dark .bp3-html-select option, .bp3-dark
  .bp3-select option{
    background-color:#30404d;
    color:#f5f8fa; }
  .bp3-dark .bp3-html-select option:disabled, .bp3-dark
  .bp3-select option:disabled{
    color:rgba(167, 182, 194, 0.6); }
  .bp3-dark .bp3-html-select::after, .bp3-dark
  .bp3-select::after{
    color:#a7b6c2; }

.bp3-select::after{
  font-family:"Icons16", sans-serif;
  font-size:16px;
  font-style:normal;
  font-weight:400;
  line-height:1;
  -moz-osx-font-smoothing:grayscale;
  -webkit-font-smoothing:antialiased;
  content:""; }
.bp3-running-text table, table.bp3-html-table{
  border-spacing:0;
  font-size:14px; }
  .bp3-running-text table th, table.bp3-html-table th,
  .bp3-running-text table td,
  table.bp3-html-table td{
    padding:11px;
    text-align:left;
    vertical-align:top; }
  .bp3-running-text table th, table.bp3-html-table th{
    color:#182026;
    font-weight:600; }
  
  .bp3-running-text table td,
  table.bp3-html-table td{
    color:#182026; }
  .bp3-running-text table tbody tr:first-child th, table.bp3-html-table tbody tr:first-child th,
  .bp3-running-text table tbody tr:first-child td,
  table.bp3-html-table tbody tr:first-child td,
  .bp3-running-text table tfoot tr:first-child th,
  table.bp3-html-table tfoot tr:first-child th,
  .bp3-running-text table tfoot tr:first-child td,
  table.bp3-html-table tfoot tr:first-child td{
    -webkit-box-shadow:inset 0 1px 0 0 rgba(16, 22, 26, 0.15);
            box-shadow:inset 0 1px 0 0 rgba(16, 22, 26, 0.15); }
  .bp3-dark .bp3-running-text table th, .bp3-running-text .bp3-dark table th, .bp3-dark table.bp3-html-table th{
    color:#f5f8fa; }
  .bp3-dark .bp3-running-text table td, .bp3-running-text .bp3-dark table td, .bp3-dark table.bp3-html-table td{
    color:#f5f8fa; }
  .bp3-dark .bp3-running-text table tbody tr:first-child th, .bp3-running-text .bp3-dark table tbody tr:first-child th, .bp3-dark table.bp3-html-table tbody tr:first-child th,
  .bp3-dark .bp3-running-text table tbody tr:first-child td,
  .bp3-running-text .bp3-dark table tbody tr:first-child td,
  .bp3-dark table.bp3-html-table tbody tr:first-child td,
  .bp3-dark .bp3-running-text table tfoot tr:first-child th,
  .bp3-running-text .bp3-dark table tfoot tr:first-child th,
  .bp3-dark table.bp3-html-table tfoot tr:first-child th,
  .bp3-dark .bp3-running-text table tfoot tr:first-child td,
  .bp3-running-text .bp3-dark table tfoot tr:first-child td,
  .bp3-dark table.bp3-html-table tfoot tr:first-child td{
    -webkit-box-shadow:inset 0 1px 0 0 rgba(255, 255, 255, 0.15);
            box-shadow:inset 0 1px 0 0 rgba(255, 255, 255, 0.15); }

table.bp3-html-table.bp3-html-table-condensed th,
table.bp3-html-table.bp3-html-table-condensed td, table.bp3-html-table.bp3-small th,
table.bp3-html-table.bp3-small td{
  padding-bottom:6px;
  padding-top:6px; }

table.bp3-html-table.bp3-html-table-striped tbody tr:nth-child(odd) td{
  background:rgba(191, 204, 214, 0.15); }

table.bp3-html-table.bp3-html-table-bordered th:not(:first-child){
  -webkit-box-shadow:inset 1px 0 0 0 rgba(16, 22, 26, 0.15);
          box-shadow:inset 1px 0 0 0 rgba(16, 22, 26, 0.15); }

table.bp3-html-table.bp3-html-table-bordered tbody tr td,
table.bp3-html-table.bp3-html-table-bordered tfoot tr td{
  -webkit-box-shadow:inset 0 1px 0 0 rgba(16, 22, 26, 0.15);
          box-shadow:inset 0 1px 0 0 rgba(16, 22, 26, 0.15); }
  table.bp3-html-table.bp3-html-table-bordered tbody tr td:not(:first-child),
  table.bp3-html-table.bp3-html-table-bordered tfoot tr td:not(:first-child){
    -webkit-box-shadow:inset 1px 1px 0 0 rgba(16, 22, 26, 0.15);
            box-shadow:inset 1px 1px 0 0 rgba(16, 22, 26, 0.15); }

table.bp3-html-table.bp3-html-table-bordered.bp3-html-table-striped tbody tr:not(:first-child) td{
  -webkit-box-shadow:none;
          box-shadow:none; }
  table.bp3-html-table.bp3-html-table-bordered.bp3-html-table-striped tbody tr:not(:first-child) td:not(:first-child){
    -webkit-box-shadow:inset 1px 0 0 0 rgba(16, 22, 26, 0.15);
            box-shadow:inset 1px 0 0 0 rgba(16, 22, 26, 0.15); }

table.bp3-html-table.bp3-interactive tbody tr:hover td{
  background-color:rgba(191, 204, 214, 0.3);
  cursor:pointer; }

table.bp3-html-table.bp3-interactive tbody tr:active td{
  background-color:rgba(191, 204, 214, 0.4); }

.bp3-dark table.bp3-html-table{ }
  .bp3-dark table.bp3-html-table.bp3-html-table-striped tbody tr:nth-child(odd) td{
    background:rgba(92, 112, 128, 0.15); }
  .bp3-dark table.bp3-html-table.bp3-html-table-bordered th:not(:first-child){
    -webkit-box-shadow:inset 1px 0 0 0 rgba(255, 255, 255, 0.15);
            box-shadow:inset 1px 0 0 0 rgba(255, 255, 255, 0.15); }
  .bp3-dark table.bp3-html-table.bp3-html-table-bordered tbody tr td,
  .bp3-dark table.bp3-html-table.bp3-html-table-bordered tfoot tr td{
    -webkit-box-shadow:inset 0 1px 0 0 rgba(255, 255, 255, 0.15);
            box-shadow:inset 0 1px 0 0 rgba(255, 255, 255, 0.15); }
    .bp3-dark table.bp3-html-table.bp3-html-table-bordered tbody tr td:not(:first-child),
    .bp3-dark table.bp3-html-table.bp3-html-table-bordered tfoot tr td:not(:first-child){
      -webkit-box-shadow:inset 1px 1px 0 0 rgba(255, 255, 255, 0.15);
              box-shadow:inset 1px 1px 0 0 rgba(255, 255, 255, 0.15); }
  .bp3-dark table.bp3-html-table.bp3-html-table-bordered.bp3-html-table-striped tbody tr:not(:first-child) td{
    -webkit-box-shadow:inset 1px 0 0 0 rgba(255, 255, 255, 0.15);
            box-shadow:inset 1px 0 0 0 rgba(255, 255, 255, 0.15); }
    .bp3-dark table.bp3-html-table.bp3-html-table-bordered.bp3-html-table-striped tbody tr:not(:first-child) td:first-child{
      -webkit-box-shadow:none;
              box-shadow:none; }
  .bp3-dark table.bp3-html-table.bp3-interactive tbody tr:hover td{
    background-color:rgba(92, 112, 128, 0.3);
    cursor:pointer; }
  .bp3-dark table.bp3-html-table.bp3-interactive tbody tr:active td{
    background-color:rgba(92, 112, 128, 0.4); }

.bp3-key-combo{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:normal;
      -ms-flex-direction:row;
          flex-direction:row;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center; }
  .bp3-key-combo > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-key-combo > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-key-combo::before,
  .bp3-key-combo > *{
    margin-right:5px; }
  .bp3-key-combo:empty::before,
  .bp3-key-combo > :last-child{
    margin-right:0; }

.bp3-hotkey-dialog{
  padding-bottom:0;
  top:40px; }
  .bp3-hotkey-dialog .bp3-dialog-body{
    margin:0;
    padding:0; }
  .bp3-hotkey-dialog .bp3-hotkey-label{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1; }

.bp3-hotkey-column{
  margin:auto;
  max-height:80vh;
  overflow-y:auto;
  padding:30px; }
  .bp3-hotkey-column .bp3-heading{
    margin-bottom:20px; }
    .bp3-hotkey-column .bp3-heading:not(:first-child){
      margin-top:40px; }

.bp3-hotkey{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-pack:justify;
      -ms-flex-pack:justify;
          justify-content:space-between;
  margin-left:0;
  margin-right:0; }
  .bp3-hotkey:not(:last-child){
    margin-bottom:10px; }
.bp3-icon{
  display:inline-block;
  -webkit-box-flex:0;
      -ms-flex:0 0 auto;
          flex:0 0 auto;
  vertical-align:text-bottom; }
  .bp3-icon:not(:empty)::before{
    content:"" !important;
    content:unset !important; }
  .bp3-icon > svg{
    display:block; }
    .bp3-icon > svg:not([fill]){
      fill:currentColor; }

.bp3-icon.bp3-intent-primary, .bp3-icon-standard.bp3-intent-primary, .bp3-icon-large.bp3-intent-primary{
  color:#106ba3; }
  .bp3-dark .bp3-icon.bp3-intent-primary, .bp3-dark .bp3-icon-standard.bp3-intent-primary, .bp3-dark .bp3-icon-large.bp3-intent-primary{
    color:#48aff0; }

.bp3-icon.bp3-intent-success, .bp3-icon-standard.bp3-intent-success, .bp3-icon-large.bp3-intent-success{
  color:#0d8050; }
  .bp3-dark .bp3-icon.bp3-intent-success, .bp3-dark .bp3-icon-standard.bp3-intent-success, .bp3-dark .bp3-icon-large.bp3-intent-success{
    color:#3dcc91; }

.bp3-icon.bp3-intent-warning, .bp3-icon-standard.bp3-intent-warning, .bp3-icon-large.bp3-intent-warning{
  color:#bf7326; }
  .bp3-dark .bp3-icon.bp3-intent-warning, .bp3-dark .bp3-icon-standard.bp3-intent-warning, .bp3-dark .bp3-icon-large.bp3-intent-warning{
    color:#ffb366; }

.bp3-icon.bp3-intent-danger, .bp3-icon-standard.bp3-intent-danger, .bp3-icon-large.bp3-intent-danger{
  color:#c23030; }
  .bp3-dark .bp3-icon.bp3-intent-danger, .bp3-dark .bp3-icon-standard.bp3-intent-danger, .bp3-dark .bp3-icon-large.bp3-intent-danger{
    color:#ff7373; }

span.bp3-icon-standard{
  font-family:"Icons16", sans-serif;
  font-size:16px;
  font-style:normal;
  font-weight:400;
  line-height:1;
  -moz-osx-font-smoothing:grayscale;
  -webkit-font-smoothing:antialiased;
  display:inline-block; }

span.bp3-icon-large{
  font-family:"Icons20", sans-serif;
  font-size:20px;
  font-style:normal;
  font-weight:400;
  line-height:1;
  -moz-osx-font-smoothing:grayscale;
  -webkit-font-smoothing:antialiased;
  display:inline-block; }

span.bp3-icon:empty{
  font-family:"Icons20";
  font-size:inherit;
  font-style:normal;
  font-weight:400;
  line-height:1; }
  span.bp3-icon:empty::before{
    -moz-osx-font-smoothing:grayscale;
    -webkit-font-smoothing:antialiased; }

.bp3-icon-add::before{
  content:""; }

.bp3-icon-add-column-left::before{
  content:""; }

.bp3-icon-add-column-right::before{
  content:""; }

.bp3-icon-add-row-bottom::before{
  content:""; }

.bp3-icon-add-row-top::before{
  content:""; }

.bp3-icon-add-to-artifact::before{
  content:""; }

.bp3-icon-add-to-folder::before{
  content:""; }

.bp3-icon-airplane::before{
  content:""; }

.bp3-icon-align-center::before{
  content:""; }

.bp3-icon-align-justify::before{
  content:""; }

.bp3-icon-align-left::before{
  content:""; }

.bp3-icon-align-right::before{
  content:""; }

.bp3-icon-alignment-bottom::before{
  content:""; }

.bp3-icon-alignment-horizontal-center::before{
  content:""; }

.bp3-icon-alignment-left::before{
  content:""; }

.bp3-icon-alignment-right::before{
  content:""; }

.bp3-icon-alignment-top::before{
  content:""; }

.bp3-icon-alignment-vertical-center::before{
  content:""; }

.bp3-icon-annotation::before{
  content:""; }

.bp3-icon-application::before{
  content:""; }

.bp3-icon-applications::before{
  content:""; }

.bp3-icon-archive::before{
  content:""; }

.bp3-icon-arrow-bottom-left::before{
  content:"↙"; }

.bp3-icon-arrow-bottom-right::before{
  content:"↘"; }

.bp3-icon-arrow-down::before{
  content:"↓"; }

.bp3-icon-arrow-left::before{
  content:"←"; }

.bp3-icon-arrow-right::before{
  content:"→"; }

.bp3-icon-arrow-top-left::before{
  content:"↖"; }

.bp3-icon-arrow-top-right::before{
  content:"↗"; }

.bp3-icon-arrow-up::before{
  content:"↑"; }

.bp3-icon-arrows-horizontal::before{
  content:"↔"; }

.bp3-icon-arrows-vertical::before{
  content:"↕"; }

.bp3-icon-asterisk::before{
  content:"*"; }

.bp3-icon-automatic-updates::before{
  content:""; }

.bp3-icon-badge::before{
  content:""; }

.bp3-icon-ban-circle::before{
  content:""; }

.bp3-icon-bank-account::before{
  content:""; }

.bp3-icon-barcode::before{
  content:""; }

.bp3-icon-blank::before{
  content:""; }

.bp3-icon-blocked-person::before{
  content:""; }

.bp3-icon-bold::before{
  content:""; }

.bp3-icon-book::before{
  content:""; }

.bp3-icon-bookmark::before{
  content:""; }

.bp3-icon-box::before{
  content:""; }

.bp3-icon-briefcase::before{
  content:""; }

.bp3-icon-bring-data::before{
  content:""; }

.bp3-icon-build::before{
  content:""; }

.bp3-icon-calculator::before{
  content:""; }

.bp3-icon-calendar::before{
  content:""; }

.bp3-icon-camera::before{
  content:""; }

.bp3-icon-caret-down::before{
  content:"⌄"; }

.bp3-icon-caret-left::before{
  content:"〈"; }

.bp3-icon-caret-right::before{
  content:"〉"; }

.bp3-icon-caret-up::before{
  content:"⌃"; }

.bp3-icon-cell-tower::before{
  content:""; }

.bp3-icon-changes::before{
  content:""; }

.bp3-icon-chart::before{
  content:""; }

.bp3-icon-chat::before{
  content:""; }

.bp3-icon-chevron-backward::before{
  content:""; }

.bp3-icon-chevron-down::before{
  content:""; }

.bp3-icon-chevron-forward::before{
  content:""; }

.bp3-icon-chevron-left::before{
  content:""; }

.bp3-icon-chevron-right::before{
  content:""; }

.bp3-icon-chevron-up::before{
  content:""; }

.bp3-icon-circle::before{
  content:""; }

.bp3-icon-circle-arrow-down::before{
  content:""; }

.bp3-icon-circle-arrow-left::before{
  content:""; }

.bp3-icon-circle-arrow-right::before{
  content:""; }

.bp3-icon-circle-arrow-up::before{
  content:""; }

.bp3-icon-citation::before{
  content:""; }

.bp3-icon-clean::before{
  content:""; }

.bp3-icon-clipboard::before{
  content:""; }

.bp3-icon-cloud::before{
  content:"☁"; }

.bp3-icon-cloud-download::before{
  content:""; }

.bp3-icon-cloud-upload::before{
  content:""; }

.bp3-icon-code::before{
  content:""; }

.bp3-icon-code-block::before{
  content:""; }

.bp3-icon-cog::before{
  content:""; }

.bp3-icon-collapse-all::before{
  content:""; }

.bp3-icon-column-layout::before{
  content:""; }

.bp3-icon-comment::before{
  content:""; }

.bp3-icon-comparison::before{
  content:""; }

.bp3-icon-compass::before{
  content:""; }

.bp3-icon-compressed::before{
  content:""; }

.bp3-icon-confirm::before{
  content:""; }

.bp3-icon-console::before{
  content:""; }

.bp3-icon-contrast::before{
  content:""; }

.bp3-icon-control::before{
  content:""; }

.bp3-icon-credit-card::before{
  content:""; }

.bp3-icon-cross::before{
  content:"✗"; }

.bp3-icon-crown::before{
  content:""; }

.bp3-icon-cube::before{
  content:""; }

.bp3-icon-cube-add::before{
  content:""; }

.bp3-icon-cube-remove::before{
  content:""; }

.bp3-icon-curved-range-chart::before{
  content:""; }

.bp3-icon-cut::before{
  content:""; }

.bp3-icon-dashboard::before{
  content:""; }

.bp3-icon-data-lineage::before{
  content:""; }

.bp3-icon-database::before{
  content:""; }

.bp3-icon-delete::before{
  content:""; }

.bp3-icon-delta::before{
  content:"Δ"; }

.bp3-icon-derive-column::before{
  content:""; }

.bp3-icon-desktop::before{
  content:""; }

.bp3-icon-diagnosis::before{
  content:""; }

.bp3-icon-diagram-tree::before{
  content:""; }

.bp3-icon-direction-left::before{
  content:""; }

.bp3-icon-direction-right::before{
  content:""; }

.bp3-icon-disable::before{
  content:""; }

.bp3-icon-document::before{
  content:""; }

.bp3-icon-document-open::before{
  content:""; }

.bp3-icon-document-share::before{
  content:""; }

.bp3-icon-dollar::before{
  content:"$"; }

.bp3-icon-dot::before{
  content:"•"; }

.bp3-icon-double-caret-horizontal::before{
  content:""; }

.bp3-icon-double-caret-vertical::before{
  content:""; }

.bp3-icon-double-chevron-down::before{
  content:""; }

.bp3-icon-double-chevron-left::before{
  content:""; }

.bp3-icon-double-chevron-right::before{
  content:""; }

.bp3-icon-double-chevron-up::before{
  content:""; }

.bp3-icon-doughnut-chart::before{
  content:""; }

.bp3-icon-download::before{
  content:""; }

.bp3-icon-drag-handle-horizontal::before{
  content:""; }

.bp3-icon-drag-handle-vertical::before{
  content:""; }

.bp3-icon-draw::before{
  content:""; }

.bp3-icon-drive-time::before{
  content:""; }

.bp3-icon-duplicate::before{
  content:""; }

.bp3-icon-edit::before{
  content:"✎"; }

.bp3-icon-eject::before{
  content:"⏏"; }

.bp3-icon-endorsed::before{
  content:""; }

.bp3-icon-envelope::before{
  content:"✉"; }

.bp3-icon-equals::before{
  content:""; }

.bp3-icon-eraser::before{
  content:""; }

.bp3-icon-error::before{
  content:""; }

.bp3-icon-euro::before{
  content:"€"; }

.bp3-icon-exchange::before{
  content:""; }

.bp3-icon-exclude-row::before{
  content:""; }

.bp3-icon-expand-all::before{
  content:""; }

.bp3-icon-export::before{
  content:""; }

.bp3-icon-eye-off::before{
  content:""; }

.bp3-icon-eye-on::before{
  content:""; }

.bp3-icon-eye-open::before{
  content:""; }

.bp3-icon-fast-backward::before{
  content:""; }

.bp3-icon-fast-forward::before{
  content:""; }

.bp3-icon-feed::before{
  content:""; }

.bp3-icon-feed-subscribed::before{
  content:""; }

.bp3-icon-film::before{
  content:""; }

.bp3-icon-filter::before{
  content:""; }

.bp3-icon-filter-keep::before{
  content:""; }

.bp3-icon-filter-list::before{
  content:""; }

.bp3-icon-filter-open::before{
  content:""; }

.bp3-icon-filter-remove::before{
  content:""; }

.bp3-icon-flag::before{
  content:"⚑"; }

.bp3-icon-flame::before{
  content:""; }

.bp3-icon-flash::before{
  content:""; }

.bp3-icon-floppy-disk::before{
  content:""; }

.bp3-icon-flow-branch::before{
  content:""; }

.bp3-icon-flow-end::before{
  content:""; }

.bp3-icon-flow-linear::before{
  content:""; }

.bp3-icon-flow-review::before{
  content:""; }

.bp3-icon-flow-review-branch::before{
  content:""; }

.bp3-icon-flows::before{
  content:""; }

.bp3-icon-folder-close::before{
  content:""; }

.bp3-icon-folder-new::before{
  content:""; }

.bp3-icon-folder-open::before{
  content:""; }

.bp3-icon-folder-shared::before{
  content:""; }

.bp3-icon-folder-shared-open::before{
  content:""; }

.bp3-icon-follower::before{
  content:""; }

.bp3-icon-following::before{
  content:""; }

.bp3-icon-font::before{
  content:""; }

.bp3-icon-fork::before{
  content:""; }

.bp3-icon-form::before{
  content:""; }

.bp3-icon-full-circle::before{
  content:""; }

.bp3-icon-full-stacked-chart::before{
  content:""; }

.bp3-icon-fullscreen::before{
  content:""; }

.bp3-icon-function::before{
  content:""; }

.bp3-icon-gantt-chart::before{
  content:""; }

.bp3-icon-geolocation::before{
  content:""; }

.bp3-icon-geosearch::before{
  content:""; }

.bp3-icon-git-branch::before{
  content:""; }

.bp3-icon-git-commit::before{
  content:""; }

.bp3-icon-git-merge::before{
  content:""; }

.bp3-icon-git-new-branch::before{
  content:""; }

.bp3-icon-git-pull::before{
  content:""; }

.bp3-icon-git-push::before{
  content:""; }

.bp3-icon-git-repo::before{
  content:""; }

.bp3-icon-glass::before{
  content:""; }

.bp3-icon-globe::before{
  content:""; }

.bp3-icon-globe-network::before{
  content:""; }

.bp3-icon-graph::before{
  content:""; }

.bp3-icon-graph-remove::before{
  content:""; }

.bp3-icon-greater-than::before{
  content:""; }

.bp3-icon-greater-than-or-equal-to::before{
  content:""; }

.bp3-icon-grid::before{
  content:""; }

.bp3-icon-grid-view::before{
  content:""; }

.bp3-icon-group-objects::before{
  content:""; }

.bp3-icon-grouped-bar-chart::before{
  content:""; }

.bp3-icon-hand::before{
  content:""; }

.bp3-icon-hand-down::before{
  content:""; }

.bp3-icon-hand-left::before{
  content:""; }

.bp3-icon-hand-right::before{
  content:""; }

.bp3-icon-hand-up::before{
  content:""; }

.bp3-icon-header::before{
  content:""; }

.bp3-icon-header-one::before{
  content:""; }

.bp3-icon-header-two::before{
  content:""; }

.bp3-icon-headset::before{
  content:""; }

.bp3-icon-heart::before{
  content:"♥"; }

.bp3-icon-heart-broken::before{
  content:""; }

.bp3-icon-heat-grid::before{
  content:""; }

.bp3-icon-heatmap::before{
  content:""; }

.bp3-icon-help::before{
  content:"?"; }

.bp3-icon-helper-management::before{
  content:""; }

.bp3-icon-highlight::before{
  content:""; }

.bp3-icon-history::before{
  content:""; }

.bp3-icon-home::before{
  content:"⌂"; }

.bp3-icon-horizontal-bar-chart::before{
  content:""; }

.bp3-icon-horizontal-bar-chart-asc::before{
  content:""; }

.bp3-icon-horizontal-bar-chart-desc::before{
  content:""; }

.bp3-icon-horizontal-distribution::before{
  content:""; }

.bp3-icon-id-number::before{
  content:""; }

.bp3-icon-image-rotate-left::before{
  content:""; }

.bp3-icon-image-rotate-right::before{
  content:""; }

.bp3-icon-import::before{
  content:""; }

.bp3-icon-inbox::before{
  content:""; }

.bp3-icon-inbox-filtered::before{
  content:""; }

.bp3-icon-inbox-geo::before{
  content:""; }

.bp3-icon-inbox-search::before{
  content:""; }

.bp3-icon-inbox-update::before{
  content:""; }

.bp3-icon-info-sign::before{
  content:"ℹ"; }

.bp3-icon-inheritance::before{
  content:""; }

.bp3-icon-inner-join::before{
  content:""; }

.bp3-icon-insert::before{
  content:""; }

.bp3-icon-intersection::before{
  content:""; }

.bp3-icon-ip-address::before{
  content:""; }

.bp3-icon-issue::before{
  content:""; }

.bp3-icon-issue-closed::before{
  content:""; }

.bp3-icon-issue-new::before{
  content:""; }

.bp3-icon-italic::before{
  content:""; }

.bp3-icon-join-table::before{
  content:""; }

.bp3-icon-key::before{
  content:""; }

.bp3-icon-key-backspace::before{
  content:""; }

.bp3-icon-key-command::before{
  content:""; }

.bp3-icon-key-control::before{
  content:""; }

.bp3-icon-key-delete::before{
  content:""; }

.bp3-icon-key-enter::before{
  content:""; }

.bp3-icon-key-escape::before{
  content:""; }

.bp3-icon-key-option::before{
  content:""; }

.bp3-icon-key-shift::before{
  content:""; }

.bp3-icon-key-tab::before{
  content:""; }

.bp3-icon-known-vehicle::before{
  content:""; }

.bp3-icon-lab-test::before{
  content:""; }

.bp3-icon-label::before{
  content:""; }

.bp3-icon-layer::before{
  content:""; }

.bp3-icon-layers::before{
  content:""; }

.bp3-icon-layout::before{
  content:""; }

.bp3-icon-layout-auto::before{
  content:""; }

.bp3-icon-layout-balloon::before{
  content:""; }

.bp3-icon-layout-circle::before{
  content:""; }

.bp3-icon-layout-grid::before{
  content:""; }

.bp3-icon-layout-group-by::before{
  content:""; }

.bp3-icon-layout-hierarchy::before{
  content:""; }

.bp3-icon-layout-linear::before{
  content:""; }

.bp3-icon-layout-skew-grid::before{
  content:""; }

.bp3-icon-layout-sorted-clusters::before{
  content:""; }

.bp3-icon-learning::before{
  content:""; }

.bp3-icon-left-join::before{
  content:""; }

.bp3-icon-less-than::before{
  content:""; }

.bp3-icon-less-than-or-equal-to::before{
  content:""; }

.bp3-icon-lifesaver::before{
  content:""; }

.bp3-icon-lightbulb::before{
  content:""; }

.bp3-icon-link::before{
  content:""; }

.bp3-icon-list::before{
  content:"☰"; }

.bp3-icon-list-columns::before{
  content:""; }

.bp3-icon-list-detail-view::before{
  content:""; }

.bp3-icon-locate::before{
  content:""; }

.bp3-icon-lock::before{
  content:""; }

.bp3-icon-log-in::before{
  content:""; }

.bp3-icon-log-out::before{
  content:""; }

.bp3-icon-manual::before{
  content:""; }

.bp3-icon-manually-entered-data::before{
  content:""; }

.bp3-icon-map::before{
  content:""; }

.bp3-icon-map-create::before{
  content:""; }

.bp3-icon-map-marker::before{
  content:""; }

.bp3-icon-maximize::before{
  content:""; }

.bp3-icon-media::before{
  content:""; }

.bp3-icon-menu::before{
  content:""; }

.bp3-icon-menu-closed::before{
  content:""; }

.bp3-icon-menu-open::before{
  content:""; }

.bp3-icon-merge-columns::before{
  content:""; }

.bp3-icon-merge-links::before{
  content:""; }

.bp3-icon-minimize::before{
  content:""; }

.bp3-icon-minus::before{
  content:"−"; }

.bp3-icon-mobile-phone::before{
  content:""; }

.bp3-icon-mobile-video::before{
  content:""; }

.bp3-icon-moon::before{
  content:""; }

.bp3-icon-more::before{
  content:""; }

.bp3-icon-mountain::before{
  content:""; }

.bp3-icon-move::before{
  content:""; }

.bp3-icon-mugshot::before{
  content:""; }

.bp3-icon-multi-select::before{
  content:""; }

.bp3-icon-music::before{
  content:""; }

.bp3-icon-new-drawing::before{
  content:""; }

.bp3-icon-new-grid-item::before{
  content:""; }

.bp3-icon-new-layer::before{
  content:""; }

.bp3-icon-new-layers::before{
  content:""; }

.bp3-icon-new-link::before{
  content:""; }

.bp3-icon-new-object::before{
  content:""; }

.bp3-icon-new-person::before{
  content:""; }

.bp3-icon-new-prescription::before{
  content:""; }

.bp3-icon-new-text-box::before{
  content:""; }

.bp3-icon-ninja::before{
  content:""; }

.bp3-icon-not-equal-to::before{
  content:""; }

.bp3-icon-notifications::before{
  content:""; }

.bp3-icon-notifications-updated::before{
  content:""; }

.bp3-icon-numbered-list::before{
  content:""; }

.bp3-icon-numerical::before{
  content:""; }

.bp3-icon-office::before{
  content:""; }

.bp3-icon-offline::before{
  content:""; }

.bp3-icon-oil-field::before{
  content:""; }

.bp3-icon-one-column::before{
  content:""; }

.bp3-icon-outdated::before{
  content:""; }

.bp3-icon-page-layout::before{
  content:""; }

.bp3-icon-panel-stats::before{
  content:""; }

.bp3-icon-panel-table::before{
  content:""; }

.bp3-icon-paperclip::before{
  content:""; }

.bp3-icon-paragraph::before{
  content:""; }

.bp3-icon-path::before{
  content:""; }

.bp3-icon-path-search::before{
  content:""; }

.bp3-icon-pause::before{
  content:""; }

.bp3-icon-people::before{
  content:""; }

.bp3-icon-percentage::before{
  content:""; }

.bp3-icon-person::before{
  content:""; }

.bp3-icon-phone::before{
  content:"☎"; }

.bp3-icon-pie-chart::before{
  content:""; }

.bp3-icon-pin::before{
  content:""; }

.bp3-icon-pivot::before{
  content:""; }

.bp3-icon-pivot-table::before{
  content:""; }

.bp3-icon-play::before{
  content:""; }

.bp3-icon-plus::before{
  content:"+"; }

.bp3-icon-polygon-filter::before{
  content:""; }

.bp3-icon-power::before{
  content:""; }

.bp3-icon-predictive-analysis::before{
  content:""; }

.bp3-icon-prescription::before{
  content:""; }

.bp3-icon-presentation::before{
  content:""; }

.bp3-icon-print::before{
  content:"⎙"; }

.bp3-icon-projects::before{
  content:""; }

.bp3-icon-properties::before{
  content:""; }

.bp3-icon-property::before{
  content:""; }

.bp3-icon-publish-function::before{
  content:""; }

.bp3-icon-pulse::before{
  content:""; }

.bp3-icon-random::before{
  content:""; }

.bp3-icon-record::before{
  content:""; }

.bp3-icon-redo::before{
  content:""; }

.bp3-icon-refresh::before{
  content:""; }

.bp3-icon-regression-chart::before{
  content:""; }

.bp3-icon-remove::before{
  content:""; }

.bp3-icon-remove-column::before{
  content:""; }

.bp3-icon-remove-column-left::before{
  content:""; }

.bp3-icon-remove-column-right::before{
  content:""; }

.bp3-icon-remove-row-bottom::before{
  content:""; }

.bp3-icon-remove-row-top::before{
  content:""; }

.bp3-icon-repeat::before{
  content:""; }

.bp3-icon-reset::before{
  content:""; }

.bp3-icon-resolve::before{
  content:""; }

.bp3-icon-rig::before{
  content:""; }

.bp3-icon-right-join::before{
  content:""; }

.bp3-icon-ring::before{
  content:""; }

.bp3-icon-rotate-document::before{
  content:""; }

.bp3-icon-rotate-page::before{
  content:""; }

.bp3-icon-satellite::before{
  content:""; }

.bp3-icon-saved::before{
  content:""; }

.bp3-icon-scatter-plot::before{
  content:""; }

.bp3-icon-search::before{
  content:""; }

.bp3-icon-search-around::before{
  content:""; }

.bp3-icon-search-template::before{
  content:""; }

.bp3-icon-search-text::before{
  content:""; }

.bp3-icon-segmented-control::before{
  content:""; }

.bp3-icon-select::before{
  content:""; }

.bp3-icon-selection::before{
  content:"⦿"; }

.bp3-icon-send-to::before{
  content:""; }

.bp3-icon-send-to-graph::before{
  content:""; }

.bp3-icon-send-to-map::before{
  content:""; }

.bp3-icon-series-add::before{
  content:""; }

.bp3-icon-series-configuration::before{
  content:""; }

.bp3-icon-series-derived::before{
  content:""; }

.bp3-icon-series-filtered::before{
  content:""; }

.bp3-icon-series-search::before{
  content:""; }

.bp3-icon-settings::before{
  content:""; }

.bp3-icon-share::before{
  content:""; }

.bp3-icon-shield::before{
  content:""; }

.bp3-icon-shop::before{
  content:""; }

.bp3-icon-shopping-cart::before{
  content:""; }

.bp3-icon-signal-search::before{
  content:""; }

.bp3-icon-sim-card::before{
  content:""; }

.bp3-icon-slash::before{
  content:""; }

.bp3-icon-small-cross::before{
  content:""; }

.bp3-icon-small-minus::before{
  content:""; }

.bp3-icon-small-plus::before{
  content:""; }

.bp3-icon-small-tick::before{
  content:""; }

.bp3-icon-snowflake::before{
  content:""; }

.bp3-icon-social-media::before{
  content:""; }

.bp3-icon-sort::before{
  content:""; }

.bp3-icon-sort-alphabetical::before{
  content:""; }

.bp3-icon-sort-alphabetical-desc::before{
  content:""; }

.bp3-icon-sort-asc::before{
  content:""; }

.bp3-icon-sort-desc::before{
  content:""; }

.bp3-icon-sort-numerical::before{
  content:""; }

.bp3-icon-sort-numerical-desc::before{
  content:""; }

.bp3-icon-split-columns::before{
  content:""; }

.bp3-icon-square::before{
  content:""; }

.bp3-icon-stacked-chart::before{
  content:""; }

.bp3-icon-star::before{
  content:"★"; }

.bp3-icon-star-empty::before{
  content:"☆"; }

.bp3-icon-step-backward::before{
  content:""; }

.bp3-icon-step-chart::before{
  content:""; }

.bp3-icon-step-forward::before{
  content:""; }

.bp3-icon-stop::before{
  content:""; }

.bp3-icon-stopwatch::before{
  content:""; }

.bp3-icon-strikethrough::before{
  content:""; }

.bp3-icon-style::before{
  content:""; }

.bp3-icon-swap-horizontal::before{
  content:""; }

.bp3-icon-swap-vertical::before{
  content:""; }

.bp3-icon-symbol-circle::before{
  content:""; }

.bp3-icon-symbol-cross::before{
  content:""; }

.bp3-icon-symbol-diamond::before{
  content:""; }

.bp3-icon-symbol-square::before{
  content:""; }

.bp3-icon-symbol-triangle-down::before{
  content:""; }

.bp3-icon-symbol-triangle-up::before{
  content:""; }

.bp3-icon-tag::before{
  content:""; }

.bp3-icon-take-action::before{
  content:""; }

.bp3-icon-taxi::before{
  content:""; }

.bp3-icon-text-highlight::before{
  content:""; }

.bp3-icon-th::before{
  content:""; }

.bp3-icon-th-derived::before{
  content:""; }

.bp3-icon-th-disconnect::before{
  content:""; }

.bp3-icon-th-filtered::before{
  content:""; }

.bp3-icon-th-list::before{
  content:""; }

.bp3-icon-thumbs-down::before{
  content:""; }

.bp3-icon-thumbs-up::before{
  content:""; }

.bp3-icon-tick::before{
  content:"✓"; }

.bp3-icon-tick-circle::before{
  content:""; }

.bp3-icon-time::before{
  content:"⏲"; }

.bp3-icon-timeline-area-chart::before{
  content:""; }

.bp3-icon-timeline-bar-chart::before{
  content:""; }

.bp3-icon-timeline-events::before{
  content:""; }

.bp3-icon-timeline-line-chart::before{
  content:""; }

.bp3-icon-tint::before{
  content:""; }

.bp3-icon-torch::before{
  content:""; }

.bp3-icon-tractor::before{
  content:""; }

.bp3-icon-train::before{
  content:""; }

.bp3-icon-translate::before{
  content:""; }

.bp3-icon-trash::before{
  content:""; }

.bp3-icon-tree::before{
  content:""; }

.bp3-icon-trending-down::before{
  content:""; }

.bp3-icon-trending-up::before{
  content:""; }

.bp3-icon-truck::before{
  content:""; }

.bp3-icon-two-columns::before{
  content:""; }

.bp3-icon-unarchive::before{
  content:""; }

.bp3-icon-underline::before{
  content:"⎁"; }

.bp3-icon-undo::before{
  content:"⎌"; }

.bp3-icon-ungroup-objects::before{
  content:""; }

.bp3-icon-unknown-vehicle::before{
  content:""; }

.bp3-icon-unlock::before{
  content:""; }

.bp3-icon-unpin::before{
  content:""; }

.bp3-icon-unresolve::before{
  content:""; }

.bp3-icon-updated::before{
  content:""; }

.bp3-icon-upload::before{
  content:""; }

.bp3-icon-user::before{
  content:""; }

.bp3-icon-variable::before{
  content:""; }

.bp3-icon-vertical-bar-chart-asc::before{
  content:""; }

.bp3-icon-vertical-bar-chart-desc::before{
  content:""; }

.bp3-icon-vertical-distribution::before{
  content:""; }

.bp3-icon-video::before{
  content:""; }

.bp3-icon-volume-down::before{
  content:""; }

.bp3-icon-volume-off::before{
  content:""; }

.bp3-icon-volume-up::before{
  content:""; }

.bp3-icon-walk::before{
  content:""; }

.bp3-icon-warning-sign::before{
  content:""; }

.bp3-icon-waterfall-chart::before{
  content:""; }

.bp3-icon-widget::before{
  content:""; }

.bp3-icon-widget-button::before{
  content:""; }

.bp3-icon-widget-footer::before{
  content:""; }

.bp3-icon-widget-header::before{
  content:""; }

.bp3-icon-wrench::before{
  content:""; }

.bp3-icon-zoom-in::before{
  content:""; }

.bp3-icon-zoom-out::before{
  content:""; }

.bp3-icon-zoom-to-fit::before{
  content:""; }
.bp3-submenu > .bp3-popover-wrapper{
  display:block; }

.bp3-submenu .bp3-popover-target{
  display:block; }
  .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-menu-item{ }

.bp3-submenu.bp3-popover{
  -webkit-box-shadow:none;
          box-shadow:none;
  padding:0 5px; }
  .bp3-submenu.bp3-popover > .bp3-popover-content{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2); }
  .bp3-dark .bp3-submenu.bp3-popover, .bp3-submenu.bp3-popover.bp3-dark{
    -webkit-box-shadow:none;
            box-shadow:none; }
    .bp3-dark .bp3-submenu.bp3-popover > .bp3-popover-content, .bp3-submenu.bp3-popover.bp3-dark > .bp3-popover-content{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4); }
.bp3-menu{
  background:#ffffff;
  border-radius:3px;
  color:#182026;
  list-style:none;
  margin:0;
  min-width:180px;
  padding:5px;
  text-align:left; }

.bp3-menu-divider{
  border-top:1px solid rgba(16, 22, 26, 0.15);
  display:block;
  margin:5px; }
  .bp3-dark .bp3-menu-divider{
    border-top-color:rgba(255, 255, 255, 0.15); }

.bp3-menu-item{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:normal;
      -ms-flex-direction:row;
          flex-direction:row;
  -webkit-box-align:start;
      -ms-flex-align:start;
          align-items:flex-start;
  border-radius:2px;
  color:inherit;
  line-height:20px;
  padding:5px 7px;
  text-decoration:none;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none; }
  .bp3-menu-item > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-menu-item > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-menu-item::before,
  .bp3-menu-item > *{
    margin-right:7px; }
  .bp3-menu-item:empty::before,
  .bp3-menu-item > :last-child{
    margin-right:0; }
  .bp3-menu-item > .bp3-fill{
    word-break:break-word; }
  .bp3-menu-item:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-menu-item{
    background-color:rgba(167, 182, 194, 0.3);
    cursor:pointer;
    text-decoration:none; }
  .bp3-menu-item.bp3-disabled{
    background-color:inherit;
    color:rgba(92, 112, 128, 0.6);
    cursor:not-allowed; }
  .bp3-dark .bp3-menu-item{
    color:inherit; }
    .bp3-dark .bp3-menu-item:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-menu-item{
      background-color:rgba(138, 155, 168, 0.15);
      color:inherit; }
    .bp3-dark .bp3-menu-item.bp3-disabled{
      background-color:inherit;
      color:rgba(167, 182, 194, 0.6); }
  .bp3-menu-item.bp3-intent-primary{
    color:#106ba3; }
    .bp3-menu-item.bp3-intent-primary .bp3-icon{
      color:inherit; }
    .bp3-menu-item.bp3-intent-primary::before, .bp3-menu-item.bp3-intent-primary::after,
    .bp3-menu-item.bp3-intent-primary .bp3-menu-item-label{
      color:#106ba3; }
    .bp3-menu-item.bp3-intent-primary:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item, .bp3-menu-item.bp3-intent-primary.bp3-active{
      background-color:#137cbd; }
    .bp3-menu-item.bp3-intent-primary:active{
      background-color:#106ba3; }
    .bp3-menu-item.bp3-intent-primary:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item, .bp3-menu-item.bp3-intent-primary:hover::before, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item::before, .bp3-menu-item.bp3-intent-primary:hover::after, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item::after,
    .bp3-menu-item.bp3-intent-primary:hover .bp3-menu-item-label,
    .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item .bp3-menu-item-label, .bp3-menu-item.bp3-intent-primary:active, .bp3-menu-item.bp3-intent-primary:active::before, .bp3-menu-item.bp3-intent-primary:active::after,
    .bp3-menu-item.bp3-intent-primary:active .bp3-menu-item-label, .bp3-menu-item.bp3-intent-primary.bp3-active, .bp3-menu-item.bp3-intent-primary.bp3-active::before, .bp3-menu-item.bp3-intent-primary.bp3-active::after,
    .bp3-menu-item.bp3-intent-primary.bp3-active .bp3-menu-item-label{
      color:#ffffff; }
  .bp3-menu-item.bp3-intent-success{
    color:#0d8050; }
    .bp3-menu-item.bp3-intent-success .bp3-icon{
      color:inherit; }
    .bp3-menu-item.bp3-intent-success::before, .bp3-menu-item.bp3-intent-success::after,
    .bp3-menu-item.bp3-intent-success .bp3-menu-item-label{
      color:#0d8050; }
    .bp3-menu-item.bp3-intent-success:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item, .bp3-menu-item.bp3-intent-success.bp3-active{
      background-color:#0f9960; }
    .bp3-menu-item.bp3-intent-success:active{
      background-color:#0d8050; }
    .bp3-menu-item.bp3-intent-success:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item, .bp3-menu-item.bp3-intent-success:hover::before, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item::before, .bp3-menu-item.bp3-intent-success:hover::after, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item::after,
    .bp3-menu-item.bp3-intent-success:hover .bp3-menu-item-label,
    .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item .bp3-menu-item-label, .bp3-menu-item.bp3-intent-success:active, .bp3-menu-item.bp3-intent-success:active::before, .bp3-menu-item.bp3-intent-success:active::after,
    .bp3-menu-item.bp3-intent-success:active .bp3-menu-item-label, .bp3-menu-item.bp3-intent-success.bp3-active, .bp3-menu-item.bp3-intent-success.bp3-active::before, .bp3-menu-item.bp3-intent-success.bp3-active::after,
    .bp3-menu-item.bp3-intent-success.bp3-active .bp3-menu-item-label{
      color:#ffffff; }
  .bp3-menu-item.bp3-intent-warning{
    color:#bf7326; }
    .bp3-menu-item.bp3-intent-warning .bp3-icon{
      color:inherit; }
    .bp3-menu-item.bp3-intent-warning::before, .bp3-menu-item.bp3-intent-warning::after,
    .bp3-menu-item.bp3-intent-warning .bp3-menu-item-label{
      color:#bf7326; }
    .bp3-menu-item.bp3-intent-warning:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item, .bp3-menu-item.bp3-intent-warning.bp3-active{
      background-color:#d9822b; }
    .bp3-menu-item.bp3-intent-warning:active{
      background-color:#bf7326; }
    .bp3-menu-item.bp3-intent-warning:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item, .bp3-menu-item.bp3-intent-warning:hover::before, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item::before, .bp3-menu-item.bp3-intent-warning:hover::after, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item::after,
    .bp3-menu-item.bp3-intent-warning:hover .bp3-menu-item-label,
    .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item .bp3-menu-item-label, .bp3-menu-item.bp3-intent-warning:active, .bp3-menu-item.bp3-intent-warning:active::before, .bp3-menu-item.bp3-intent-warning:active::after,
    .bp3-menu-item.bp3-intent-warning:active .bp3-menu-item-label, .bp3-menu-item.bp3-intent-warning.bp3-active, .bp3-menu-item.bp3-intent-warning.bp3-active::before, .bp3-menu-item.bp3-intent-warning.bp3-active::after,
    .bp3-menu-item.bp3-intent-warning.bp3-active .bp3-menu-item-label{
      color:#ffffff; }
  .bp3-menu-item.bp3-intent-danger{
    color:#c23030; }
    .bp3-menu-item.bp3-intent-danger .bp3-icon{
      color:inherit; }
    .bp3-menu-item.bp3-intent-danger::before, .bp3-menu-item.bp3-intent-danger::after,
    .bp3-menu-item.bp3-intent-danger .bp3-menu-item-label{
      color:#c23030; }
    .bp3-menu-item.bp3-intent-danger:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item, .bp3-menu-item.bp3-intent-danger.bp3-active{
      background-color:#db3737; }
    .bp3-menu-item.bp3-intent-danger:active{
      background-color:#c23030; }
    .bp3-menu-item.bp3-intent-danger:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item, .bp3-menu-item.bp3-intent-danger:hover::before, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item::before, .bp3-menu-item.bp3-intent-danger:hover::after, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item::after,
    .bp3-menu-item.bp3-intent-danger:hover .bp3-menu-item-label,
    .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item .bp3-menu-item-label, .bp3-menu-item.bp3-intent-danger:active, .bp3-menu-item.bp3-intent-danger:active::before, .bp3-menu-item.bp3-intent-danger:active::after,
    .bp3-menu-item.bp3-intent-danger:active .bp3-menu-item-label, .bp3-menu-item.bp3-intent-danger.bp3-active, .bp3-menu-item.bp3-intent-danger.bp3-active::before, .bp3-menu-item.bp3-intent-danger.bp3-active::after,
    .bp3-menu-item.bp3-intent-danger.bp3-active .bp3-menu-item-label{
      color:#ffffff; }
  .bp3-menu-item::before{
    font-family:"Icons16", sans-serif;
    font-size:16px;
    font-style:normal;
    font-weight:400;
    line-height:1;
    -moz-osx-font-smoothing:grayscale;
    -webkit-font-smoothing:antialiased;
    margin-right:7px; }
  .bp3-menu-item::before,
  .bp3-menu-item > .bp3-icon{
    color:#5c7080;
    margin-top:2px; }
  .bp3-menu-item .bp3-menu-item-label{
    color:#5c7080; }
  .bp3-menu-item:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-menu-item{
    color:inherit; }
  .bp3-menu-item.bp3-active, .bp3-menu-item:active{
    background-color:rgba(115, 134, 148, 0.3); }
  .bp3-menu-item.bp3-disabled{
    background-color:inherit !important;
    color:rgba(92, 112, 128, 0.6) !important;
    cursor:not-allowed !important;
    outline:none !important; }
    .bp3-menu-item.bp3-disabled::before,
    .bp3-menu-item.bp3-disabled > .bp3-icon,
    .bp3-menu-item.bp3-disabled .bp3-menu-item-label{
      color:rgba(92, 112, 128, 0.6) !important; }
  .bp3-large .bp3-menu-item{
    font-size:16px;
    line-height:22px;
    padding:9px 7px; }
    .bp3-large .bp3-menu-item .bp3-icon{
      margin-top:3px; }
    .bp3-large .bp3-menu-item::before{
      font-family:"Icons20", sans-serif;
      font-size:20px;
      font-style:normal;
      font-weight:400;
      line-height:1;
      -moz-osx-font-smoothing:grayscale;
      -webkit-font-smoothing:antialiased;
      margin-right:10px;
      margin-top:1px; }

button.bp3-menu-item{
  background:none;
  border:none;
  text-align:left;
  width:100%; }
.bp3-menu-header{
  border-top:1px solid rgba(16, 22, 26, 0.15);
  display:block;
  margin:5px;
  cursor:default;
  padding-left:2px; }
  .bp3-dark .bp3-menu-header{
    border-top-color:rgba(255, 255, 255, 0.15); }
  .bp3-menu-header:first-of-type{
    border-top:none; }
  .bp3-menu-header > h6{
    color:#182026;
    font-weight:600;
    overflow:hidden;
    text-overflow:ellipsis;
    white-space:nowrap;
    word-wrap:normal;
    line-height:17px;
    margin:0;
    padding:10px 7px 0 1px; }
    .bp3-dark .bp3-menu-header > h6{
      color:#f5f8fa; }
  .bp3-menu-header:first-of-type > h6{
    padding-top:0; }
  .bp3-large .bp3-menu-header > h6{
    font-size:18px;
    padding-bottom:5px;
    padding-top:15px; }
  .bp3-large .bp3-menu-header:first-of-type > h6{
    padding-top:0; }

.bp3-dark .bp3-menu{
  background:#30404d;
  color:#f5f8fa; }

.bp3-dark .bp3-menu-item{ }
  .bp3-dark .bp3-menu-item.bp3-intent-primary{
    color:#48aff0; }
    .bp3-dark .bp3-menu-item.bp3-intent-primary .bp3-icon{
      color:inherit; }
    .bp3-dark .bp3-menu-item.bp3-intent-primary::before, .bp3-dark .bp3-menu-item.bp3-intent-primary::after,
    .bp3-dark .bp3-menu-item.bp3-intent-primary .bp3-menu-item-label{
      color:#48aff0; }
    .bp3-dark .bp3-menu-item.bp3-intent-primary:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-primary.bp3-active{
      background-color:#137cbd; }
    .bp3-dark .bp3-menu-item.bp3-intent-primary:active{
      background-color:#106ba3; }
    .bp3-dark .bp3-menu-item.bp3-intent-primary:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-primary:hover::before, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item::before, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item::before, .bp3-dark .bp3-menu-item.bp3-intent-primary:hover::after, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item::after, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item::after,
    .bp3-dark .bp3-menu-item.bp3-intent-primary:hover .bp3-menu-item-label,
    .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item .bp3-menu-item-label,
    .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-primary:active, .bp3-dark .bp3-menu-item.bp3-intent-primary:active::before, .bp3-dark .bp3-menu-item.bp3-intent-primary:active::after,
    .bp3-dark .bp3-menu-item.bp3-intent-primary:active .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-primary.bp3-active, .bp3-dark .bp3-menu-item.bp3-intent-primary.bp3-active::before, .bp3-dark .bp3-menu-item.bp3-intent-primary.bp3-active::after,
    .bp3-dark .bp3-menu-item.bp3-intent-primary.bp3-active .bp3-menu-item-label{
      color:#ffffff; }
  .bp3-dark .bp3-menu-item.bp3-intent-success{
    color:#3dcc91; }
    .bp3-dark .bp3-menu-item.bp3-intent-success .bp3-icon{
      color:inherit; }
    .bp3-dark .bp3-menu-item.bp3-intent-success::before, .bp3-dark .bp3-menu-item.bp3-intent-success::after,
    .bp3-dark .bp3-menu-item.bp3-intent-success .bp3-menu-item-label{
      color:#3dcc91; }
    .bp3-dark .bp3-menu-item.bp3-intent-success:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-success.bp3-active{
      background-color:#0f9960; }
    .bp3-dark .bp3-menu-item.bp3-intent-success:active{
      background-color:#0d8050; }
    .bp3-dark .bp3-menu-item.bp3-intent-success:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-success:hover::before, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item::before, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item::before, .bp3-dark .bp3-menu-item.bp3-intent-success:hover::after, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item::after, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item::after,
    .bp3-dark .bp3-menu-item.bp3-intent-success:hover .bp3-menu-item-label,
    .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item .bp3-menu-item-label,
    .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-success:active, .bp3-dark .bp3-menu-item.bp3-intent-success:active::before, .bp3-dark .bp3-menu-item.bp3-intent-success:active::after,
    .bp3-dark .bp3-menu-item.bp3-intent-success:active .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-success.bp3-active, .bp3-dark .bp3-menu-item.bp3-intent-success.bp3-active::before, .bp3-dark .bp3-menu-item.bp3-intent-success.bp3-active::after,
    .bp3-dark .bp3-menu-item.bp3-intent-success.bp3-active .bp3-menu-item-label{
      color:#ffffff; }
  .bp3-dark .bp3-menu-item.bp3-intent-warning{
    color:#ffb366; }
    .bp3-dark .bp3-menu-item.bp3-intent-warning .bp3-icon{
      color:inherit; }
    .bp3-dark .bp3-menu-item.bp3-intent-warning::before, .bp3-dark .bp3-menu-item.bp3-intent-warning::after,
    .bp3-dark .bp3-menu-item.bp3-intent-warning .bp3-menu-item-label{
      color:#ffb366; }
    .bp3-dark .bp3-menu-item.bp3-intent-warning:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-warning.bp3-active{
      background-color:#d9822b; }
    .bp3-dark .bp3-menu-item.bp3-intent-warning:active{
      background-color:#bf7326; }
    .bp3-dark .bp3-menu-item.bp3-intent-warning:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-warning:hover::before, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item::before, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item::before, .bp3-dark .bp3-menu-item.bp3-intent-warning:hover::after, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item::after, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item::after,
    .bp3-dark .bp3-menu-item.bp3-intent-warning:hover .bp3-menu-item-label,
    .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item .bp3-menu-item-label,
    .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-warning:active, .bp3-dark .bp3-menu-item.bp3-intent-warning:active::before, .bp3-dark .bp3-menu-item.bp3-intent-warning:active::after,
    .bp3-dark .bp3-menu-item.bp3-intent-warning:active .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-warning.bp3-active, .bp3-dark .bp3-menu-item.bp3-intent-warning.bp3-active::before, .bp3-dark .bp3-menu-item.bp3-intent-warning.bp3-active::after,
    .bp3-dark .bp3-menu-item.bp3-intent-warning.bp3-active .bp3-menu-item-label{
      color:#ffffff; }
  .bp3-dark .bp3-menu-item.bp3-intent-danger{
    color:#ff7373; }
    .bp3-dark .bp3-menu-item.bp3-intent-danger .bp3-icon{
      color:inherit; }
    .bp3-dark .bp3-menu-item.bp3-intent-danger::before, .bp3-dark .bp3-menu-item.bp3-intent-danger::after,
    .bp3-dark .bp3-menu-item.bp3-intent-danger .bp3-menu-item-label{
      color:#ff7373; }
    .bp3-dark .bp3-menu-item.bp3-intent-danger:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-danger.bp3-active{
      background-color:#db3737; }
    .bp3-dark .bp3-menu-item.bp3-intent-danger:active{
      background-color:#c23030; }
    .bp3-dark .bp3-menu-item.bp3-intent-danger:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-danger:hover::before, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item::before, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item::before, .bp3-dark .bp3-menu-item.bp3-intent-danger:hover::after, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item::after, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item::after,
    .bp3-dark .bp3-menu-item.bp3-intent-danger:hover .bp3-menu-item-label,
    .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item .bp3-menu-item-label,
    .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-danger:active, .bp3-dark .bp3-menu-item.bp3-intent-danger:active::before, .bp3-dark .bp3-menu-item.bp3-intent-danger:active::after,
    .bp3-dark .bp3-menu-item.bp3-intent-danger:active .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-danger.bp3-active, .bp3-dark .bp3-menu-item.bp3-intent-danger.bp3-active::before, .bp3-dark .bp3-menu-item.bp3-intent-danger.bp3-active::after,
    .bp3-dark .bp3-menu-item.bp3-intent-danger.bp3-active .bp3-menu-item-label{
      color:#ffffff; }
  .bp3-dark .bp3-menu-item::before,
  .bp3-dark .bp3-menu-item > .bp3-icon{
    color:#a7b6c2; }
  .bp3-dark .bp3-menu-item .bp3-menu-item-label{
    color:#a7b6c2; }
  .bp3-dark .bp3-menu-item.bp3-active, .bp3-dark .bp3-menu-item:active{
    background-color:rgba(138, 155, 168, 0.3); }
  .bp3-dark .bp3-menu-item.bp3-disabled{
    color:rgba(167, 182, 194, 0.6) !important; }
    .bp3-dark .bp3-menu-item.bp3-disabled::before,
    .bp3-dark .bp3-menu-item.bp3-disabled > .bp3-icon,
    .bp3-dark .bp3-menu-item.bp3-disabled .bp3-menu-item-label{
      color:rgba(167, 182, 194, 0.6) !important; }

.bp3-dark .bp3-menu-divider,
.bp3-dark .bp3-menu-header{
  border-color:rgba(255, 255, 255, 0.15); }

.bp3-dark .bp3-menu-header > h6{
  color:#f5f8fa; }

.bp3-label .bp3-menu{
  margin-top:5px; }
.bp3-navbar{
  background-color:#ffffff;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2);
  height:50px;
  padding:0 15px;
  position:relative;
  width:100%;
  z-index:10; }
  .bp3-navbar.bp3-dark,
  .bp3-dark .bp3-navbar{
    background-color:#394b59; }
  .bp3-navbar.bp3-dark{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-navbar{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4); }
  .bp3-navbar.bp3-fixed-top{
    left:0;
    position:fixed;
    right:0;
    top:0; }

.bp3-navbar-heading{
  font-size:16px;
  margin-right:15px; }

.bp3-navbar-group{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  height:50px; }
  .bp3-navbar-group.bp3-align-left{
    float:left; }
  .bp3-navbar-group.bp3-align-right{
    float:right; }

.bp3-navbar-divider{
  border-left:1px solid rgba(16, 22, 26, 0.15);
  height:20px;
  margin:0 10px; }
  .bp3-dark .bp3-navbar-divider{
    border-left-color:rgba(255, 255, 255, 0.15); }
.bp3-non-ideal-state{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:vertical;
  -webkit-box-direction:normal;
      -ms-flex-direction:column;
          flex-direction:column;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  height:100%;
  -webkit-box-pack:center;
      -ms-flex-pack:center;
          justify-content:center;
  text-align:center;
  width:100%; }
  .bp3-non-ideal-state > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-non-ideal-state > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-non-ideal-state::before,
  .bp3-non-ideal-state > *{
    margin-bottom:20px; }
  .bp3-non-ideal-state:empty::before,
  .bp3-non-ideal-state > :last-child{
    margin-bottom:0; }
  .bp3-non-ideal-state > *{
    max-width:400px; }

.bp3-non-ideal-state-visual{
  color:rgba(92, 112, 128, 0.6);
  font-size:60px; }
  .bp3-dark .bp3-non-ideal-state-visual{
    color:rgba(167, 182, 194, 0.6); }

.bp3-overflow-list{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -ms-flex-wrap:nowrap;
      flex-wrap:nowrap;
  min-width:0; }

.bp3-overflow-list-spacer{
  -ms-flex-negative:1;
      flex-shrink:1;
  width:1px; }

body.bp3-overlay-open{
  overflow:hidden; }

.bp3-overlay{
  bottom:0;
  left:0;
  position:static;
  right:0;
  top:0;
  z-index:20; }
  .bp3-overlay:not(.bp3-overlay-open){
    pointer-events:none; }
  .bp3-overlay.bp3-overlay-container{
    overflow:hidden;
    position:fixed; }
    .bp3-overlay.bp3-overlay-container.bp3-overlay-inline{
      position:absolute; }
  .bp3-overlay.bp3-overlay-scroll-container{
    overflow:auto;
    position:fixed; }
    .bp3-overlay.bp3-overlay-scroll-container.bp3-overlay-inline{
      position:absolute; }
  .bp3-overlay.bp3-overlay-inline{
    display:inline;
    overflow:visible; }

.bp3-overlay-content{
  position:fixed;
  z-index:20; }
  .bp3-overlay-inline .bp3-overlay-content,
  .bp3-overlay-scroll-container .bp3-overlay-content{
    position:absolute; }

.bp3-overlay-backdrop{
  bottom:0;
  left:0;
  position:fixed;
  right:0;
  top:0;
  opacity:1;
  background-color:rgba(16, 22, 26, 0.7);
  overflow:auto;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none;
  z-index:20; }
  .bp3-overlay-backdrop.bp3-overlay-enter, .bp3-overlay-backdrop.bp3-overlay-appear{
    opacity:0; }
  .bp3-overlay-backdrop.bp3-overlay-enter-active, .bp3-overlay-backdrop.bp3-overlay-appear-active{
    opacity:1;
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:200ms;
            transition-duration:200ms;
    -webkit-transition-property:opacity;
    transition-property:opacity;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-overlay-backdrop.bp3-overlay-exit{
    opacity:1; }
  .bp3-overlay-backdrop.bp3-overlay-exit-active{
    opacity:0;
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:200ms;
            transition-duration:200ms;
    -webkit-transition-property:opacity;
    transition-property:opacity;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-overlay-backdrop:focus{
    outline:none; }
  .bp3-overlay-inline .bp3-overlay-backdrop{
    position:absolute; }
.bp3-panel-stack{
  overflow:hidden;
  position:relative; }

.bp3-panel-stack-header{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  -webkit-box-shadow:0 1px rgba(16, 22, 26, 0.15);
          box-shadow:0 1px rgba(16, 22, 26, 0.15);
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -ms-flex-negative:0;
      flex-shrink:0;
  height:30px;
  z-index:1; }
  .bp3-dark .bp3-panel-stack-header{
    -webkit-box-shadow:0 1px rgba(255, 255, 255, 0.15);
            box-shadow:0 1px rgba(255, 255, 255, 0.15); }
  .bp3-panel-stack-header > span{
    -webkit-box-align:stretch;
        -ms-flex-align:stretch;
            align-items:stretch;
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    -webkit-box-flex:1;
        -ms-flex:1;
            flex:1; }
  .bp3-panel-stack-header .bp3-heading{
    margin:0 5px; }

.bp3-button.bp3-panel-stack-header-back{
  margin-left:5px;
  padding-left:0;
  white-space:nowrap; }
  .bp3-button.bp3-panel-stack-header-back .bp3-icon{
    margin:0 2px; }

.bp3-panel-stack-view{
  bottom:0;
  left:0;
  position:absolute;
  right:0;
  top:0;
  background-color:#ffffff;
  border-right:1px solid rgba(16, 22, 26, 0.15);
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:vertical;
  -webkit-box-direction:normal;
      -ms-flex-direction:column;
          flex-direction:column;
  margin-right:-1px;
  overflow-y:auto;
  z-index:1; }
  .bp3-dark .bp3-panel-stack-view{
    background-color:#30404d; }
  .bp3-panel-stack-view:nth-last-child(n + 4){
    display:none; }

.bp3-panel-stack-push .bp3-panel-stack-enter, .bp3-panel-stack-push .bp3-panel-stack-appear{
  -webkit-transform:translateX(100%);
          transform:translateX(100%);
  opacity:0; }

.bp3-panel-stack-push .bp3-panel-stack-enter-active, .bp3-panel-stack-push .bp3-panel-stack-appear-active{
  -webkit-transform:translate(0%);
          transform:translate(0%);
  opacity:1;
  -webkit-transition-delay:0;
          transition-delay:0;
  -webkit-transition-duration:400ms;
          transition-duration:400ms;
  -webkit-transition-property:opacity, -webkit-transform;
  transition-property:opacity, -webkit-transform;
  transition-property:transform, opacity;
  transition-property:transform, opacity, -webkit-transform;
  -webkit-transition-timing-function:ease;
          transition-timing-function:ease; }

.bp3-panel-stack-push .bp3-panel-stack-exit{
  -webkit-transform:translate(0%);
          transform:translate(0%);
  opacity:1; }

.bp3-panel-stack-push .bp3-panel-stack-exit-active{
  -webkit-transform:translateX(-50%);
          transform:translateX(-50%);
  opacity:0;
  -webkit-transition-delay:0;
          transition-delay:0;
  -webkit-transition-duration:400ms;
          transition-duration:400ms;
  -webkit-transition-property:opacity, -webkit-transform;
  transition-property:opacity, -webkit-transform;
  transition-property:transform, opacity;
  transition-property:transform, opacity, -webkit-transform;
  -webkit-transition-timing-function:ease;
          transition-timing-function:ease; }

.bp3-panel-stack-pop .bp3-panel-stack-enter, .bp3-panel-stack-pop .bp3-panel-stack-appear{
  -webkit-transform:translateX(-50%);
          transform:translateX(-50%);
  opacity:0; }

.bp3-panel-stack-pop .bp3-panel-stack-enter-active, .bp3-panel-stack-pop .bp3-panel-stack-appear-active{
  -webkit-transform:translate(0%);
          transform:translate(0%);
  opacity:1;
  -webkit-transition-delay:0;
          transition-delay:0;
  -webkit-transition-duration:400ms;
          transition-duration:400ms;
  -webkit-transition-property:opacity, -webkit-transform;
  transition-property:opacity, -webkit-transform;
  transition-property:transform, opacity;
  transition-property:transform, opacity, -webkit-transform;
  -webkit-transition-timing-function:ease;
          transition-timing-function:ease; }

.bp3-panel-stack-pop .bp3-panel-stack-exit{
  -webkit-transform:translate(0%);
          transform:translate(0%);
  opacity:1; }

.bp3-panel-stack-pop .bp3-panel-stack-exit-active{
  -webkit-transform:translateX(100%);
          transform:translateX(100%);
  opacity:0;
  -webkit-transition-delay:0;
          transition-delay:0;
  -webkit-transition-duration:400ms;
          transition-duration:400ms;
  -webkit-transition-property:opacity, -webkit-transform;
  transition-property:opacity, -webkit-transform;
  transition-property:transform, opacity;
  transition-property:transform, opacity, -webkit-transform;
  -webkit-transition-timing-function:ease;
          transition-timing-function:ease; }
.bp3-panel-stack2{
  overflow:hidden;
  position:relative; }

.bp3-panel-stack2-header{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  -webkit-box-shadow:0 1px rgba(16, 22, 26, 0.15);
          box-shadow:0 1px rgba(16, 22, 26, 0.15);
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -ms-flex-negative:0;
      flex-shrink:0;
  height:30px;
  z-index:1; }
  .bp3-dark .bp3-panel-stack2-header{
    -webkit-box-shadow:0 1px rgba(255, 255, 255, 0.15);
            box-shadow:0 1px rgba(255, 255, 255, 0.15); }
  .bp3-panel-stack2-header > span{
    -webkit-box-align:stretch;
        -ms-flex-align:stretch;
            align-items:stretch;
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    -webkit-box-flex:1;
        -ms-flex:1;
            flex:1; }
  .bp3-panel-stack2-header .bp3-heading{
    margin:0 5px; }

.bp3-button.bp3-panel-stack2-header-back{
  margin-left:5px;
  padding-left:0;
  white-space:nowrap; }
  .bp3-button.bp3-panel-stack2-header-back .bp3-icon{
    margin:0 2px; }

.bp3-panel-stack2-view{
  bottom:0;
  left:0;
  position:absolute;
  right:0;
  top:0;
  background-color:#ffffff;
  border-right:1px solid rgba(16, 22, 26, 0.15);
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:vertical;
  -webkit-box-direction:normal;
      -ms-flex-direction:column;
          flex-direction:column;
  margin-right:-1px;
  overflow-y:auto;
  z-index:1; }
  .bp3-dark .bp3-panel-stack2-view{
    background-color:#30404d; }
  .bp3-panel-stack2-view:nth-last-child(n + 4){
    display:none; }

.bp3-panel-stack2-push .bp3-panel-stack2-enter, .bp3-panel-stack2-push .bp3-panel-stack2-appear{
  -webkit-transform:translateX(100%);
          transform:translateX(100%);
  opacity:0; }

.bp3-panel-stack2-push .bp3-panel-stack2-enter-active, .bp3-panel-stack2-push .bp3-panel-stack2-appear-active{
  -webkit-transform:translate(0%);
          transform:translate(0%);
  opacity:1;
  -webkit-transition-delay:0;
          transition-delay:0;
  -webkit-transition-duration:400ms;
          transition-duration:400ms;
  -webkit-transition-property:opacity, -webkit-transform;
  transition-property:opacity, -webkit-transform;
  transition-property:transform, opacity;
  transition-property:transform, opacity, -webkit-transform;
  -webkit-transition-timing-function:ease;
          transition-timing-function:ease; }

.bp3-panel-stack2-push .bp3-panel-stack2-exit{
  -webkit-transform:translate(0%);
          transform:translate(0%);
  opacity:1; }

.bp3-panel-stack2-push .bp3-panel-stack2-exit-active{
  -webkit-transform:translateX(-50%);
          transform:translateX(-50%);
  opacity:0;
  -webkit-transition-delay:0;
          transition-delay:0;
  -webkit-transition-duration:400ms;
          transition-duration:400ms;
  -webkit-transition-property:opacity, -webkit-transform;
  transition-property:opacity, -webkit-transform;
  transition-property:transform, opacity;
  transition-property:transform, opacity, -webkit-transform;
  -webkit-transition-timing-function:ease;
          transition-timing-function:ease; }

.bp3-panel-stack2-pop .bp3-panel-stack2-enter, .bp3-panel-stack2-pop .bp3-panel-stack2-appear{
  -webkit-transform:translateX(-50%);
          transform:translateX(-50%);
  opacity:0; }

.bp3-panel-stack2-pop .bp3-panel-stack2-enter-active, .bp3-panel-stack2-pop .bp3-panel-stack2-appear-active{
  -webkit-transform:translate(0%);
          transform:translate(0%);
  opacity:1;
  -webkit-transition-delay:0;
          transition-delay:0;
  -webkit-transition-duration:400ms;
          transition-duration:400ms;
  -webkit-transition-property:opacity, -webkit-transform;
  transition-property:opacity, -webkit-transform;
  transition-property:transform, opacity;
  transition-property:transform, opacity, -webkit-transform;
  -webkit-transition-timing-function:ease;
          transition-timing-function:ease; }

.bp3-panel-stack2-pop .bp3-panel-stack2-exit{
  -webkit-transform:translate(0%);
          transform:translate(0%);
  opacity:1; }

.bp3-panel-stack2-pop .bp3-panel-stack2-exit-active{
  -webkit-transform:translateX(100%);
          transform:translateX(100%);
  opacity:0;
  -webkit-transition-delay:0;
          transition-delay:0;
  -webkit-transition-duration:400ms;
          transition-duration:400ms;
  -webkit-transition-property:opacity, -webkit-transform;
  transition-property:opacity, -webkit-transform;
  transition-property:transform, opacity;
  transition-property:transform, opacity, -webkit-transform;
  -webkit-transition-timing-function:ease;
          transition-timing-function:ease; }
.bp3-popover{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
  -webkit-transform:scale(1);
          transform:scale(1);
  border-radius:3px;
  display:inline-block;
  z-index:20; }
  .bp3-popover .bp3-popover-arrow{
    height:30px;
    position:absolute;
    width:30px; }
    .bp3-popover .bp3-popover-arrow::before{
      height:20px;
      margin:5px;
      width:20px; }
  .bp3-tether-element-attached-bottom.bp3-tether-target-attached-top > .bp3-popover{
    margin-bottom:17px;
    margin-top:-17px; }
    .bp3-tether-element-attached-bottom.bp3-tether-target-attached-top > .bp3-popover > .bp3-popover-arrow{
      bottom:-11px; }
      .bp3-tether-element-attached-bottom.bp3-tether-target-attached-top > .bp3-popover > .bp3-popover-arrow svg{
        -webkit-transform:rotate(-90deg);
                transform:rotate(-90deg); }
  .bp3-tether-element-attached-left.bp3-tether-target-attached-right > .bp3-popover{
    margin-left:17px; }
    .bp3-tether-element-attached-left.bp3-tether-target-attached-right > .bp3-popover > .bp3-popover-arrow{
      left:-11px; }
      .bp3-tether-element-attached-left.bp3-tether-target-attached-right > .bp3-popover > .bp3-popover-arrow svg{
        -webkit-transform:rotate(0);
                transform:rotate(0); }
  .bp3-tether-element-attached-top.bp3-tether-target-attached-bottom > .bp3-popover{
    margin-top:17px; }
    .bp3-tether-element-attached-top.bp3-tether-target-attached-bottom > .bp3-popover > .bp3-popover-arrow{
      top:-11px; }
      .bp3-tether-element-attached-top.bp3-tether-target-attached-bottom > .bp3-popover > .bp3-popover-arrow svg{
        -webkit-transform:rotate(90deg);
                transform:rotate(90deg); }
  .bp3-tether-element-attached-right.bp3-tether-target-attached-left > .bp3-popover{
    margin-left:-17px;
    margin-right:17px; }
    .bp3-tether-element-attached-right.bp3-tether-target-attached-left > .bp3-popover > .bp3-popover-arrow{
      right:-11px; }
      .bp3-tether-element-attached-right.bp3-tether-target-attached-left > .bp3-popover > .bp3-popover-arrow svg{
        -webkit-transform:rotate(180deg);
                transform:rotate(180deg); }
  .bp3-tether-element-attached-middle > .bp3-popover > .bp3-popover-arrow{
    top:50%;
    -webkit-transform:translateY(-50%);
            transform:translateY(-50%); }
  .bp3-tether-element-attached-center > .bp3-popover > .bp3-popover-arrow{
    right:50%;
    -webkit-transform:translateX(50%);
            transform:translateX(50%); }
  .bp3-tether-element-attached-top.bp3-tether-target-attached-top > .bp3-popover > .bp3-popover-arrow{
    top:-0.3934px; }
  .bp3-tether-element-attached-right.bp3-tether-target-attached-right > .bp3-popover > .bp3-popover-arrow{
    right:-0.3934px; }
  .bp3-tether-element-attached-left.bp3-tether-target-attached-left > .bp3-popover > .bp3-popover-arrow{
    left:-0.3934px; }
  .bp3-tether-element-attached-bottom.bp3-tether-target-attached-bottom > .bp3-popover > .bp3-popover-arrow{
    bottom:-0.3934px; }
  .bp3-tether-element-attached-top.bp3-tether-element-attached-left > .bp3-popover{
    -webkit-transform-origin:top left;
            transform-origin:top left; }
  .bp3-tether-element-attached-top.bp3-tether-element-attached-center > .bp3-popover{
    -webkit-transform-origin:top center;
            transform-origin:top center; }
  .bp3-tether-element-attached-top.bp3-tether-element-attached-right > .bp3-popover{
    -webkit-transform-origin:top right;
            transform-origin:top right; }
  .bp3-tether-element-attached-middle.bp3-tether-element-attached-left > .bp3-popover{
    -webkit-transform-origin:center left;
            transform-origin:center left; }
  .bp3-tether-element-attached-middle.bp3-tether-element-attached-center > .bp3-popover{
    -webkit-transform-origin:center center;
            transform-origin:center center; }
  .bp3-tether-element-attached-middle.bp3-tether-element-attached-right > .bp3-popover{
    -webkit-transform-origin:center right;
            transform-origin:center right; }
  .bp3-tether-element-attached-bottom.bp3-tether-element-attached-left > .bp3-popover{
    -webkit-transform-origin:bottom left;
            transform-origin:bottom left; }
  .bp3-tether-element-attached-bottom.bp3-tether-element-attached-center > .bp3-popover{
    -webkit-transform-origin:bottom center;
            transform-origin:bottom center; }
  .bp3-tether-element-attached-bottom.bp3-tether-element-attached-right > .bp3-popover{
    -webkit-transform-origin:bottom right;
            transform-origin:bottom right; }
  .bp3-popover .bp3-popover-content{
    background:#ffffff;
    color:inherit; }
  .bp3-popover .bp3-popover-arrow::before{
    -webkit-box-shadow:1px 1px 6px rgba(16, 22, 26, 0.2);
            box-shadow:1px 1px 6px rgba(16, 22, 26, 0.2); }
  .bp3-popover .bp3-popover-arrow-border{
    fill:#10161a;
    fill-opacity:0.1; }
  .bp3-popover .bp3-popover-arrow-fill{
    fill:#ffffff; }
  .bp3-popover-enter > .bp3-popover, .bp3-popover-appear > .bp3-popover{
    -webkit-transform:scale(0.3);
            transform:scale(0.3); }
  .bp3-popover-enter-active > .bp3-popover, .bp3-popover-appear-active > .bp3-popover{
    -webkit-transform:scale(1);
            transform:scale(1);
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:300ms;
            transition-duration:300ms;
    -webkit-transition-property:-webkit-transform;
    transition-property:-webkit-transform;
    transition-property:transform;
    transition-property:transform, -webkit-transform;
    -webkit-transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
            transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11); }
  .bp3-popover-exit > .bp3-popover{
    -webkit-transform:scale(1);
            transform:scale(1); }
  .bp3-popover-exit-active > .bp3-popover{
    -webkit-transform:scale(0.3);
            transform:scale(0.3);
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:300ms;
            transition-duration:300ms;
    -webkit-transition-property:-webkit-transform;
    transition-property:-webkit-transform;
    transition-property:transform;
    transition-property:transform, -webkit-transform;
    -webkit-transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
            transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11); }
  .bp3-popover .bp3-popover-content{
    border-radius:3px;
    position:relative; }
  .bp3-popover.bp3-popover-content-sizing .bp3-popover-content{
    max-width:350px;
    padding:20px; }
  .bp3-popover-target + .bp3-overlay .bp3-popover.bp3-popover-content-sizing{
    width:350px; }
  .bp3-popover.bp3-minimal{
    margin:0 !important; }
    .bp3-popover.bp3-minimal .bp3-popover-arrow{
      display:none; }
    .bp3-popover.bp3-minimal.bp3-popover{
      -webkit-transform:scale(1);
              transform:scale(1); }
      .bp3-popover-enter > .bp3-popover.bp3-minimal.bp3-popover, .bp3-popover-appear > .bp3-popover.bp3-minimal.bp3-popover{
        -webkit-transform:scale(1);
                transform:scale(1); }
      .bp3-popover-enter-active > .bp3-popover.bp3-minimal.bp3-popover, .bp3-popover-appear-active > .bp3-popover.bp3-minimal.bp3-popover{
        -webkit-transform:scale(1);
                transform:scale(1);
        -webkit-transition-delay:0;
                transition-delay:0;
        -webkit-transition-duration:100ms;
                transition-duration:100ms;
        -webkit-transition-property:-webkit-transform;
        transition-property:-webkit-transform;
        transition-property:transform;
        transition-property:transform, -webkit-transform;
        -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
                transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
      .bp3-popover-exit > .bp3-popover.bp3-minimal.bp3-popover{
        -webkit-transform:scale(1);
                transform:scale(1); }
      .bp3-popover-exit-active > .bp3-popover.bp3-minimal.bp3-popover{
        -webkit-transform:scale(1);
                transform:scale(1);
        -webkit-transition-delay:0;
                transition-delay:0;
        -webkit-transition-duration:100ms;
                transition-duration:100ms;
        -webkit-transition-property:-webkit-transform;
        transition-property:-webkit-transform;
        transition-property:transform;
        transition-property:transform, -webkit-transform;
        -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
                transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-popover.bp3-dark,
  .bp3-dark .bp3-popover{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4); }
    .bp3-popover.bp3-dark .bp3-popover-content,
    .bp3-dark .bp3-popover .bp3-popover-content{
      background:#30404d;
      color:inherit; }
    .bp3-popover.bp3-dark .bp3-popover-arrow::before,
    .bp3-dark .bp3-popover .bp3-popover-arrow::before{
      -webkit-box-shadow:1px 1px 6px rgba(16, 22, 26, 0.4);
              box-shadow:1px 1px 6px rgba(16, 22, 26, 0.4); }
    .bp3-popover.bp3-dark .bp3-popover-arrow-border,
    .bp3-dark .bp3-popover .bp3-popover-arrow-border{
      fill:#10161a;
      fill-opacity:0.2; }
    .bp3-popover.bp3-dark .bp3-popover-arrow-fill,
    .bp3-dark .bp3-popover .bp3-popover-arrow-fill{
      fill:#30404d; }

.bp3-popover-arrow::before{
  border-radius:2px;
  content:"";
  display:block;
  position:absolute;
  -webkit-transform:rotate(45deg);
          transform:rotate(45deg); }

.bp3-tether-pinned .bp3-popover-arrow{
  display:none; }

.bp3-popover-backdrop{
  background:rgba(255, 255, 255, 0); }

.bp3-transition-container{
  opacity:1;
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  z-index:20; }
  .bp3-transition-container.bp3-popover-enter, .bp3-transition-container.bp3-popover-appear{
    opacity:0; }
  .bp3-transition-container.bp3-popover-enter-active, .bp3-transition-container.bp3-popover-appear-active{
    opacity:1;
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:100ms;
            transition-duration:100ms;
    -webkit-transition-property:opacity;
    transition-property:opacity;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-transition-container.bp3-popover-exit{
    opacity:1; }
  .bp3-transition-container.bp3-popover-exit-active{
    opacity:0;
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:100ms;
            transition-duration:100ms;
    -webkit-transition-property:opacity;
    transition-property:opacity;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-transition-container:focus{
    outline:none; }
  .bp3-transition-container.bp3-popover-leave .bp3-popover-content{
    pointer-events:none; }
  .bp3-transition-container[data-x-out-of-boundaries]{
    display:none; }

span.bp3-popover-target{
  display:inline-block; }

.bp3-popover-wrapper.bp3-fill{
  width:100%; }

.bp3-portal{
  left:0;
  position:absolute;
  right:0;
  top:0; }
@-webkit-keyframes linear-progress-bar-stripes{
  from{
    background-position:0 0; }
  to{
    background-position:30px 0; } }
@keyframes linear-progress-bar-stripes{
  from{
    background-position:0 0; }
  to{
    background-position:30px 0; } }

.bp3-progress-bar{
  background:rgba(92, 112, 128, 0.2);
  border-radius:40px;
  display:block;
  height:8px;
  overflow:hidden;
  position:relative;
  width:100%; }
  .bp3-progress-bar .bp3-progress-meter{
    background:linear-gradient(-45deg, rgba(255, 255, 255, 0.2) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.2) 50%, rgba(255, 255, 255, 0.2) 75%, transparent 75%);
    background-color:rgba(92, 112, 128, 0.8);
    background-size:30px 30px;
    border-radius:40px;
    height:100%;
    position:absolute;
    -webkit-transition:width 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:width 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
    width:100%; }
  .bp3-progress-bar:not(.bp3-no-animation):not(.bp3-no-stripes) .bp3-progress-meter{
    animation:linear-progress-bar-stripes 300ms linear infinite reverse; }
  .bp3-progress-bar.bp3-no-stripes .bp3-progress-meter{
    background-image:none; }

.bp3-dark .bp3-progress-bar{
  background:rgba(16, 22, 26, 0.5); }
  .bp3-dark .bp3-progress-bar .bp3-progress-meter{
    background-color:#8a9ba8; }

.bp3-progress-bar.bp3-intent-primary .bp3-progress-meter{
  background-color:#137cbd; }

.bp3-progress-bar.bp3-intent-success .bp3-progress-meter{
  background-color:#0f9960; }

.bp3-progress-bar.bp3-intent-warning .bp3-progress-meter{
  background-color:#d9822b; }

.bp3-progress-bar.bp3-intent-danger .bp3-progress-meter{
  background-color:#db3737; }
@-webkit-keyframes skeleton-glow{
  from{
    background:rgba(206, 217, 224, 0.2);
    border-color:rgba(206, 217, 224, 0.2); }
  to{
    background:rgba(92, 112, 128, 0.2);
    border-color:rgba(92, 112, 128, 0.2); } }
@keyframes skeleton-glow{
  from{
    background:rgba(206, 217, 224, 0.2);
    border-color:rgba(206, 217, 224, 0.2); }
  to{
    background:rgba(92, 112, 128, 0.2);
    border-color:rgba(92, 112, 128, 0.2); } }
.bp3-skeleton{
  -webkit-animation:1000ms linear infinite alternate skeleton-glow;
          animation:1000ms linear infinite alternate skeleton-glow;
  background:rgba(206, 217, 224, 0.2);
  background-clip:padding-box !important;
  border-color:rgba(206, 217, 224, 0.2) !important;
  border-radius:2px;
  -webkit-box-shadow:none !important;
          box-shadow:none !important;
  color:transparent !important;
  cursor:default;
  pointer-events:none;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none; }
  .bp3-skeleton::before, .bp3-skeleton::after,
  .bp3-skeleton *{
    visibility:hidden !important; }
.bp3-slider{
  height:40px;
  min-width:150px;
  width:100%;
  cursor:default;
  outline:none;
  position:relative;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none; }
  .bp3-slider:hover{
    cursor:pointer; }
  .bp3-slider:active{
    cursor:-webkit-grabbing;
    cursor:grabbing; }
  .bp3-slider.bp3-disabled{
    cursor:not-allowed;
    opacity:0.5; }
  .bp3-slider.bp3-slider-unlabeled{
    height:16px; }

.bp3-slider-track,
.bp3-slider-progress{
  height:6px;
  left:0;
  right:0;
  top:5px;
  position:absolute; }

.bp3-slider-track{
  border-radius:3px;
  overflow:hidden; }

.bp3-slider-progress{
  background:rgba(92, 112, 128, 0.2); }
  .bp3-dark .bp3-slider-progress{
    background:rgba(16, 22, 26, 0.5); }
  .bp3-slider-progress.bp3-intent-primary{
    background-color:#137cbd; }
  .bp3-slider-progress.bp3-intent-success{
    background-color:#0f9960; }
  .bp3-slider-progress.bp3-intent-warning{
    background-color:#d9822b; }
  .bp3-slider-progress.bp3-intent-danger{
    background-color:#db3737; }

.bp3-slider-handle{
  background-color:#f5f8fa;
  background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.8)), to(rgba(255, 255, 255, 0)));
  background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.8), rgba(255, 255, 255, 0));
  -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
          box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
  color:#182026;
  border-radius:3px;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.2);
  cursor:pointer;
  height:16px;
  left:0;
  position:absolute;
  top:0;
  width:16px; }
  .bp3-slider-handle:hover{
    background-clip:padding-box;
    background-color:#ebf1f5;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1); }
  .bp3-slider-handle:active, .bp3-slider-handle.bp3-active{
    background-color:#d8e1e8;
    background-image:none;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
  .bp3-slider-handle:disabled, .bp3-slider-handle.bp3-disabled{
    background-color:rgba(206, 217, 224, 0.5);
    background-image:none;
    -webkit-box-shadow:none;
            box-shadow:none;
    color:rgba(92, 112, 128, 0.6);
    cursor:not-allowed;
    outline:none; }
    .bp3-slider-handle:disabled.bp3-active, .bp3-slider-handle:disabled.bp3-active:hover, .bp3-slider-handle.bp3-disabled.bp3-active, .bp3-slider-handle.bp3-disabled.bp3-active:hover{
      background:rgba(206, 217, 224, 0.7); }
  .bp3-slider-handle:focus{
    z-index:1; }
  .bp3-slider-handle:hover{
    background-clip:padding-box;
    background-color:#ebf1f5;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.2);
    cursor:-webkit-grab;
    cursor:grab;
    z-index:2; }
  .bp3-slider-handle.bp3-active{
    background-color:#d8e1e8;
    background-image:none;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 1px rgba(16, 22, 26, 0.1);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 1px rgba(16, 22, 26, 0.1);
    cursor:-webkit-grabbing;
    cursor:grabbing; }
  .bp3-disabled .bp3-slider-handle{
    background:#bfccd6;
    -webkit-box-shadow:none;
            box-shadow:none;
    pointer-events:none; }
  .bp3-dark .bp3-slider-handle{
    background-color:#394b59;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.05)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.05), rgba(255, 255, 255, 0));
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
    color:#f5f8fa; }
    .bp3-dark .bp3-slider-handle:hover, .bp3-dark .bp3-slider-handle:active, .bp3-dark .bp3-slider-handle.bp3-active{
      color:#f5f8fa; }
    .bp3-dark .bp3-slider-handle:hover{
      background-color:#30404d;
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-slider-handle:active, .bp3-dark .bp3-slider-handle.bp3-active{
      background-color:#202b33;
      background-image:none;
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
    .bp3-dark .bp3-slider-handle:disabled, .bp3-dark .bp3-slider-handle.bp3-disabled{
      background-color:rgba(57, 75, 89, 0.5);
      background-image:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      color:rgba(167, 182, 194, 0.6); }
      .bp3-dark .bp3-slider-handle:disabled.bp3-active, .bp3-dark .bp3-slider-handle.bp3-disabled.bp3-active{
        background:rgba(57, 75, 89, 0.7); }
    .bp3-dark .bp3-slider-handle .bp3-button-spinner .bp3-spinner-head{
      background:rgba(16, 22, 26, 0.5);
      stroke:#8a9ba8; }
    .bp3-dark .bp3-slider-handle, .bp3-dark .bp3-slider-handle:hover{
      background-color:#394b59; }
    .bp3-dark .bp3-slider-handle.bp3-active{
      background-color:#293742; }
  .bp3-dark .bp3-disabled .bp3-slider-handle{
    background:#5c7080;
    border-color:#5c7080;
    -webkit-box-shadow:none;
            box-shadow:none; }
  .bp3-slider-handle .bp3-slider-label{
    background:#394b59;
    border-radius:3px;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
    color:#f5f8fa;
    margin-left:8px; }
    .bp3-dark .bp3-slider-handle .bp3-slider-label{
      background:#e1e8ed;
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
      color:#394b59; }
    .bp3-disabled .bp3-slider-handle .bp3-slider-label{
      -webkit-box-shadow:none;
              box-shadow:none; }
  .bp3-slider-handle.bp3-start, .bp3-slider-handle.bp3-end{
    width:8px; }
  .bp3-slider-handle.bp3-start{
    border-bottom-right-radius:0;
    border-top-right-radius:0; }
  .bp3-slider-handle.bp3-end{
    border-bottom-left-radius:0;
    border-top-left-radius:0;
    margin-left:8px; }
    .bp3-slider-handle.bp3-end .bp3-slider-label{
      margin-left:0; }

.bp3-slider-label{
  -webkit-transform:translate(-50%, 20px);
          transform:translate(-50%, 20px);
  display:inline-block;
  font-size:12px;
  line-height:1;
  padding:2px 5px;
  position:absolute;
  vertical-align:top; }

.bp3-slider.bp3-vertical{
  height:150px;
  min-width:40px;
  width:40px; }
  .bp3-slider.bp3-vertical .bp3-slider-track,
  .bp3-slider.bp3-vertical .bp3-slider-progress{
    bottom:0;
    height:auto;
    left:5px;
    top:0;
    width:6px; }
  .bp3-slider.bp3-vertical .bp3-slider-progress{
    top:auto; }
  .bp3-slider.bp3-vertical .bp3-slider-label{
    -webkit-transform:translate(20px, 50%);
            transform:translate(20px, 50%); }
  .bp3-slider.bp3-vertical .bp3-slider-handle{
    top:auto; }
    .bp3-slider.bp3-vertical .bp3-slider-handle .bp3-slider-label{
      margin-left:0;
      margin-top:-8px; }
    .bp3-slider.bp3-vertical .bp3-slider-handle.bp3-end, .bp3-slider.bp3-vertical .bp3-slider-handle.bp3-start{
      height:8px;
      margin-left:0;
      width:16px; }
    .bp3-slider.bp3-vertical .bp3-slider-handle.bp3-start{
      border-bottom-right-radius:3px;
      border-top-left-radius:0; }
      .bp3-slider.bp3-vertical .bp3-slider-handle.bp3-start .bp3-slider-label{
        -webkit-transform:translate(20px);
                transform:translate(20px); }
    .bp3-slider.bp3-vertical .bp3-slider-handle.bp3-end{
      border-bottom-left-radius:0;
      border-bottom-right-radius:0;
      border-top-left-radius:3px;
      margin-bottom:8px; }

@-webkit-keyframes pt-spinner-animation{
  from{
    -webkit-transform:rotate(0deg);
            transform:rotate(0deg); }
  to{
    -webkit-transform:rotate(360deg);
            transform:rotate(360deg); } }

@keyframes pt-spinner-animation{
  from{
    -webkit-transform:rotate(0deg);
            transform:rotate(0deg); }
  to{
    -webkit-transform:rotate(360deg);
            transform:rotate(360deg); } }

.bp3-spinner{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-pack:center;
      -ms-flex-pack:center;
          justify-content:center;
  overflow:visible;
  vertical-align:middle; }
  .bp3-spinner svg{
    display:block; }
  .bp3-spinner path{
    fill-opacity:0; }
  .bp3-spinner .bp3-spinner-head{
    stroke:rgba(92, 112, 128, 0.8);
    stroke-linecap:round;
    -webkit-transform-origin:center;
            transform-origin:center;
    -webkit-transition:stroke-dashoffset 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:stroke-dashoffset 200ms cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-spinner .bp3-spinner-track{
    stroke:rgba(92, 112, 128, 0.2); }

.bp3-spinner-animation{
  -webkit-animation:pt-spinner-animation 500ms linear infinite;
          animation:pt-spinner-animation 500ms linear infinite; }
  .bp3-no-spin > .bp3-spinner-animation{
    -webkit-animation:none;
            animation:none; }

.bp3-dark .bp3-spinner .bp3-spinner-head{
  stroke:#8a9ba8; }

.bp3-dark .bp3-spinner .bp3-spinner-track{
  stroke:rgba(16, 22, 26, 0.5); }

.bp3-spinner.bp3-intent-primary .bp3-spinner-head{
  stroke:#137cbd; }

.bp3-spinner.bp3-intent-success .bp3-spinner-head{
  stroke:#0f9960; }

.bp3-spinner.bp3-intent-warning .bp3-spinner-head{
  stroke:#d9822b; }

.bp3-spinner.bp3-intent-danger .bp3-spinner-head{
  stroke:#db3737; }
.bp3-tabs.bp3-vertical{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex; }
  .bp3-tabs.bp3-vertical > .bp3-tab-list{
    -webkit-box-align:start;
        -ms-flex-align:start;
            align-items:flex-start;
    -webkit-box-orient:vertical;
    -webkit-box-direction:normal;
        -ms-flex-direction:column;
            flex-direction:column; }
    .bp3-tabs.bp3-vertical > .bp3-tab-list .bp3-tab{
      border-radius:3px;
      padding:0 10px;
      width:100%; }
      .bp3-tabs.bp3-vertical > .bp3-tab-list .bp3-tab[aria-selected="true"]{
        background-color:rgba(19, 124, 189, 0.2);
        -webkit-box-shadow:none;
                box-shadow:none; }
    .bp3-tabs.bp3-vertical > .bp3-tab-list .bp3-tab-indicator-wrapper .bp3-tab-indicator{
      background-color:rgba(19, 124, 189, 0.2);
      border-radius:3px;
      bottom:0;
      height:auto;
      left:0;
      right:0;
      top:0; }
  .bp3-tabs.bp3-vertical > .bp3-tab-panel{
    margin-top:0;
    padding-left:20px; }

.bp3-tab-list{
  -webkit-box-align:end;
      -ms-flex-align:end;
          align-items:flex-end;
  border:none;
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-flex:0;
      -ms-flex:0 0 auto;
          flex:0 0 auto;
  list-style:none;
  margin:0;
  padding:0;
  position:relative; }
  .bp3-tab-list > *:not(:last-child){
    margin-right:20px; }

.bp3-tab{
  overflow:hidden;
  text-overflow:ellipsis;
  white-space:nowrap;
  word-wrap:normal;
  color:#182026;
  cursor:pointer;
  -webkit-box-flex:0;
      -ms-flex:0 0 auto;
          flex:0 0 auto;
  font-size:14px;
  line-height:30px;
  max-width:100%;
  position:relative;
  vertical-align:top; }
  .bp3-tab a{
    color:inherit;
    display:block;
    text-decoration:none; }
  .bp3-tab-indicator-wrapper ~ .bp3-tab{
    background-color:transparent !important;
    -webkit-box-shadow:none !important;
            box-shadow:none !important; }
  .bp3-tab[aria-disabled="true"]{
    color:rgba(92, 112, 128, 0.6);
    cursor:not-allowed; }
  .bp3-tab[aria-selected="true"]{
    border-radius:0;
    -webkit-box-shadow:inset 0 -3px 0 #106ba3;
            box-shadow:inset 0 -3px 0 #106ba3; }
  .bp3-tab[aria-selected="true"], .bp3-tab:not([aria-disabled="true"]):hover{
    color:#106ba3; }
  .bp3-tab:focus{
    -moz-outline-radius:0; }
  .bp3-large > .bp3-tab{
    font-size:16px;
    line-height:40px; }

.bp3-tab-panel{
  margin-top:20px; }
  .bp3-tab-panel[aria-hidden="true"]{
    display:none; }

.bp3-tab-indicator-wrapper{
  left:0;
  pointer-events:none;
  position:absolute;
  top:0;
  -webkit-transform:translateX(0), translateY(0);
          transform:translateX(0), translateY(0);
  -webkit-transition:height, width, -webkit-transform;
  transition:height, width, -webkit-transform;
  transition:height, transform, width;
  transition:height, transform, width, -webkit-transform;
  -webkit-transition-duration:200ms;
          transition-duration:200ms;
  -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
          transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-tab-indicator-wrapper .bp3-tab-indicator{
    background-color:#106ba3;
    bottom:0;
    height:3px;
    left:0;
    position:absolute;
    right:0; }
  .bp3-tab-indicator-wrapper.bp3-no-animation{
    -webkit-transition:none;
    transition:none; }

.bp3-dark .bp3-tab{
  color:#f5f8fa; }
  .bp3-dark .bp3-tab[aria-disabled="true"]{
    color:rgba(167, 182, 194, 0.6); }
  .bp3-dark .bp3-tab[aria-selected="true"]{
    -webkit-box-shadow:inset 0 -3px 0 #48aff0;
            box-shadow:inset 0 -3px 0 #48aff0; }
  .bp3-dark .bp3-tab[aria-selected="true"], .bp3-dark .bp3-tab:not([aria-disabled="true"]):hover{
    color:#48aff0; }

.bp3-dark .bp3-tab-indicator{
  background-color:#48aff0; }

.bp3-flex-expander{
  -webkit-box-flex:1;
      -ms-flex:1 1;
          flex:1 1; }
.bp3-tag{
  display:-webkit-inline-box;
  display:-ms-inline-flexbox;
  display:inline-flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:normal;
      -ms-flex-direction:row;
          flex-direction:row;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  background-color:#5c7080;
  border:none;
  border-radius:3px;
  -webkit-box-shadow:none;
          box-shadow:none;
  color:#f5f8fa;
  font-size:12px;
  line-height:16px;
  max-width:100%;
  min-height:20px;
  min-width:20px;
  padding:2px 6px;
  position:relative; }
  .bp3-tag.bp3-interactive{
    cursor:pointer; }
    .bp3-tag.bp3-interactive:hover{
      background-color:rgba(92, 112, 128, 0.85); }
    .bp3-tag.bp3-interactive.bp3-active, .bp3-tag.bp3-interactive:active{
      background-color:rgba(92, 112, 128, 0.7); }
  .bp3-tag > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-tag > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-tag::before,
  .bp3-tag > *{
    margin-right:4px; }
  .bp3-tag:empty::before,
  .bp3-tag > :last-child{
    margin-right:0; }
  .bp3-tag:focus{
    outline:rgba(19, 124, 189, 0.6) auto 2px;
    outline-offset:0;
    -moz-outline-radius:6px; }
  .bp3-tag.bp3-round{
    border-radius:30px;
    padding-left:8px;
    padding-right:8px; }
  .bp3-dark .bp3-tag{
    background-color:#bfccd6;
    color:#182026; }
    .bp3-dark .bp3-tag.bp3-interactive{
      cursor:pointer; }
      .bp3-dark .bp3-tag.bp3-interactive:hover{
        background-color:rgba(191, 204, 214, 0.85); }
      .bp3-dark .bp3-tag.bp3-interactive.bp3-active, .bp3-dark .bp3-tag.bp3-interactive:active{
        background-color:rgba(191, 204, 214, 0.7); }
    .bp3-dark .bp3-tag > .bp3-icon, .bp3-dark .bp3-tag .bp3-icon-standard, .bp3-dark .bp3-tag .bp3-icon-large{
      fill:currentColor; }
  .bp3-tag > .bp3-icon, .bp3-tag .bp3-icon-standard, .bp3-tag .bp3-icon-large{
    fill:#ffffff; }
  .bp3-tag.bp3-large,
  .bp3-large .bp3-tag{
    font-size:14px;
    line-height:20px;
    min-height:30px;
    min-width:30px;
    padding:5px 10px; }
    .bp3-tag.bp3-large::before,
    .bp3-tag.bp3-large > *,
    .bp3-large .bp3-tag::before,
    .bp3-large .bp3-tag > *{
      margin-right:7px; }
    .bp3-tag.bp3-large:empty::before,
    .bp3-tag.bp3-large > :last-child,
    .bp3-large .bp3-tag:empty::before,
    .bp3-large .bp3-tag > :last-child{
      margin-right:0; }
    .bp3-tag.bp3-large.bp3-round,
    .bp3-large .bp3-tag.bp3-round{
      padding-left:12px;
      padding-right:12px; }
  .bp3-tag.bp3-intent-primary{
    background:#137cbd;
    color:#ffffff; }
    .bp3-tag.bp3-intent-primary.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-intent-primary.bp3-interactive:hover{
        background-color:rgba(19, 124, 189, 0.85); }
      .bp3-tag.bp3-intent-primary.bp3-interactive.bp3-active, .bp3-tag.bp3-intent-primary.bp3-interactive:active{
        background-color:rgba(19, 124, 189, 0.7); }
  .bp3-tag.bp3-intent-success{
    background:#0f9960;
    color:#ffffff; }
    .bp3-tag.bp3-intent-success.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-intent-success.bp3-interactive:hover{
        background-color:rgba(15, 153, 96, 0.85); }
      .bp3-tag.bp3-intent-success.bp3-interactive.bp3-active, .bp3-tag.bp3-intent-success.bp3-interactive:active{
        background-color:rgba(15, 153, 96, 0.7); }
  .bp3-tag.bp3-intent-warning{
    background:#d9822b;
    color:#ffffff; }
    .bp3-tag.bp3-intent-warning.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-intent-warning.bp3-interactive:hover{
        background-color:rgba(217, 130, 43, 0.85); }
      .bp3-tag.bp3-intent-warning.bp3-interactive.bp3-active, .bp3-tag.bp3-intent-warning.bp3-interactive:active{
        background-color:rgba(217, 130, 43, 0.7); }
  .bp3-tag.bp3-intent-danger{
    background:#db3737;
    color:#ffffff; }
    .bp3-tag.bp3-intent-danger.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-intent-danger.bp3-interactive:hover{
        background-color:rgba(219, 55, 55, 0.85); }
      .bp3-tag.bp3-intent-danger.bp3-interactive.bp3-active, .bp3-tag.bp3-intent-danger.bp3-interactive:active{
        background-color:rgba(219, 55, 55, 0.7); }
  .bp3-tag.bp3-fill{
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    width:100%; }
  .bp3-tag.bp3-minimal > .bp3-icon, .bp3-tag.bp3-minimal .bp3-icon-standard, .bp3-tag.bp3-minimal .bp3-icon-large{
    fill:#5c7080; }
  .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]){
    background-color:rgba(138, 155, 168, 0.2);
    color:#182026; }
    .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive:hover{
        background-color:rgba(92, 112, 128, 0.3); }
      .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive.bp3-active, .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive:active{
        background-color:rgba(92, 112, 128, 0.4); }
    .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]){
      color:#f5f8fa; }
      .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive{
        cursor:pointer; }
        .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive:hover{
          background-color:rgba(191, 204, 214, 0.3); }
        .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive.bp3-active, .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive:active{
          background-color:rgba(191, 204, 214, 0.4); }
      .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]) > .bp3-icon, .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]) .bp3-icon-standard, .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]) .bp3-icon-large{
        fill:#a7b6c2; }
  .bp3-tag.bp3-minimal.bp3-intent-primary{
    background-color:rgba(19, 124, 189, 0.15);
    color:#106ba3; }
    .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive:hover{
        background-color:rgba(19, 124, 189, 0.25); }
      .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive.bp3-active, .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive:active{
        background-color:rgba(19, 124, 189, 0.35); }
    .bp3-tag.bp3-minimal.bp3-intent-primary > .bp3-icon, .bp3-tag.bp3-minimal.bp3-intent-primary .bp3-icon-standard, .bp3-tag.bp3-minimal.bp3-intent-primary .bp3-icon-large{
      fill:#137cbd; }
    .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-primary{
      background-color:rgba(19, 124, 189, 0.25);
      color:#48aff0; }
      .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive{
        cursor:pointer; }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive:hover{
          background-color:rgba(19, 124, 189, 0.35); }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive.bp3-active, .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive:active{
          background-color:rgba(19, 124, 189, 0.45); }
  .bp3-tag.bp3-minimal.bp3-intent-success{
    background-color:rgba(15, 153, 96, 0.15);
    color:#0d8050; }
    .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive:hover{
        background-color:rgba(15, 153, 96, 0.25); }
      .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive.bp3-active, .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive:active{
        background-color:rgba(15, 153, 96, 0.35); }
    .bp3-tag.bp3-minimal.bp3-intent-success > .bp3-icon, .bp3-tag.bp3-minimal.bp3-intent-success .bp3-icon-standard, .bp3-tag.bp3-minimal.bp3-intent-success .bp3-icon-large{
      fill:#0f9960; }
    .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-success{
      background-color:rgba(15, 153, 96, 0.25);
      color:#3dcc91; }
      .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive{
        cursor:pointer; }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive:hover{
          background-color:rgba(15, 153, 96, 0.35); }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive.bp3-active, .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive:active{
          background-color:rgba(15, 153, 96, 0.45); }
  .bp3-tag.bp3-minimal.bp3-intent-warning{
    background-color:rgba(217, 130, 43, 0.15);
    color:#bf7326; }
    .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive:hover{
        background-color:rgba(217, 130, 43, 0.25); }
      .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive.bp3-active, .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive:active{
        background-color:rgba(217, 130, 43, 0.35); }
    .bp3-tag.bp3-minimal.bp3-intent-warning > .bp3-icon, .bp3-tag.bp3-minimal.bp3-intent-warning .bp3-icon-standard, .bp3-tag.bp3-minimal.bp3-intent-warning .bp3-icon-large{
      fill:#d9822b; }
    .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-warning{
      background-color:rgba(217, 130, 43, 0.25);
      color:#ffb366; }
      .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive{
        cursor:pointer; }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive:hover{
          background-color:rgba(217, 130, 43, 0.35); }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive.bp3-active, .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive:active{
          background-color:rgba(217, 130, 43, 0.45); }
  .bp3-tag.bp3-minimal.bp3-intent-danger{
    background-color:rgba(219, 55, 55, 0.15);
    color:#c23030; }
    .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive:hover{
        background-color:rgba(219, 55, 55, 0.25); }
      .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive.bp3-active, .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive:active{
        background-color:rgba(219, 55, 55, 0.35); }
    .bp3-tag.bp3-minimal.bp3-intent-danger > .bp3-icon, .bp3-tag.bp3-minimal.bp3-intent-danger .bp3-icon-standard, .bp3-tag.bp3-minimal.bp3-intent-danger .bp3-icon-large{
      fill:#db3737; }
    .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-danger{
      background-color:rgba(219, 55, 55, 0.25);
      color:#ff7373; }
      .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive{
        cursor:pointer; }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive:hover{
          background-color:rgba(219, 55, 55, 0.35); }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive.bp3-active, .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive:active{
          background-color:rgba(219, 55, 55, 0.45); }

.bp3-tag-remove{
  background:none;
  border:none;
  color:inherit;
  cursor:pointer;
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  margin-bottom:-2px;
  margin-right:-6px !important;
  margin-top:-2px;
  opacity:0.5;
  padding:2px;
  padding-left:0; }
  .bp3-tag-remove:hover{
    background:none;
    opacity:0.8;
    text-decoration:none; }
  .bp3-tag-remove:active{
    opacity:1; }
  .bp3-tag-remove:empty::before{
    font-family:"Icons16", sans-serif;
    font-size:16px;
    font-style:normal;
    font-weight:400;
    line-height:1;
    -moz-osx-font-smoothing:grayscale;
    -webkit-font-smoothing:antialiased;
    content:""; }
  .bp3-large .bp3-tag-remove{
    margin-right:-10px !important;
    padding:0 5px 0 0; }
    .bp3-large .bp3-tag-remove:empty::before{
      font-family:"Icons20", sans-serif;
      font-size:20px;
      font-style:normal;
      font-weight:400;
      line-height:1; }
.bp3-tag-input{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:normal;
      -ms-flex-direction:row;
          flex-direction:row;
  -webkit-box-align:start;
      -ms-flex-align:start;
          align-items:flex-start;
  cursor:text;
  height:auto;
  line-height:inherit;
  min-height:30px;
  padding-left:5px;
  padding-right:0; }
  .bp3-tag-input > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-tag-input > .bp3-tag-input-values{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-tag-input .bp3-tag-input-icon{
    color:#5c7080;
    margin-left:2px;
    margin-right:7px;
    margin-top:7px; }
  .bp3-tag-input .bp3-tag-input-values{
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    -webkit-box-orient:horizontal;
    -webkit-box-direction:normal;
        -ms-flex-direction:row;
            flex-direction:row;
    -webkit-box-align:center;
        -ms-flex-align:center;
            align-items:center;
    -ms-flex-item-align:stretch;
        align-self:stretch;
    -ms-flex-wrap:wrap;
        flex-wrap:wrap;
    margin-right:7px;
    margin-top:5px;
    min-width:0; }
    .bp3-tag-input .bp3-tag-input-values > *{
      -webkit-box-flex:0;
          -ms-flex-positive:0;
              flex-grow:0;
      -ms-flex-negative:0;
          flex-shrink:0; }
    .bp3-tag-input .bp3-tag-input-values > .bp3-fill{
      -webkit-box-flex:1;
          -ms-flex-positive:1;
              flex-grow:1;
      -ms-flex-negative:1;
          flex-shrink:1; }
    .bp3-tag-input .bp3-tag-input-values::before,
    .bp3-tag-input .bp3-tag-input-values > *{
      margin-right:5px; }
    .bp3-tag-input .bp3-tag-input-values:empty::before,
    .bp3-tag-input .bp3-tag-input-values > :last-child{
      margin-right:0; }
    .bp3-tag-input .bp3-tag-input-values:first-child .bp3-input-ghost:first-child{
      padding-left:5px; }
    .bp3-tag-input .bp3-tag-input-values > *{
      margin-bottom:5px; }
  .bp3-tag-input .bp3-tag{
    overflow-wrap:break-word; }
    .bp3-tag-input .bp3-tag.bp3-active{
      outline:rgba(19, 124, 189, 0.6) auto 2px;
      outline-offset:0;
      -moz-outline-radius:6px; }
  .bp3-tag-input .bp3-input-ghost{
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto;
    line-height:20px;
    width:80px; }
    .bp3-tag-input .bp3-input-ghost:disabled, .bp3-tag-input .bp3-input-ghost.bp3-disabled{
      cursor:not-allowed; }
  .bp3-tag-input .bp3-button,
  .bp3-tag-input .bp3-spinner{
    margin:3px;
    margin-left:0; }
  .bp3-tag-input .bp3-button{
    min-height:24px;
    min-width:24px;
    padding:0 7px; }
  .bp3-tag-input.bp3-large{
    height:auto;
    min-height:40px; }
    .bp3-tag-input.bp3-large::before,
    .bp3-tag-input.bp3-large > *{
      margin-right:10px; }
    .bp3-tag-input.bp3-large:empty::before,
    .bp3-tag-input.bp3-large > :last-child{
      margin-right:0; }
    .bp3-tag-input.bp3-large .bp3-tag-input-icon{
      margin-left:5px;
      margin-top:10px; }
    .bp3-tag-input.bp3-large .bp3-input-ghost{
      line-height:30px; }
    .bp3-tag-input.bp3-large .bp3-button{
      min-height:30px;
      min-width:30px;
      padding:5px 10px;
      margin:5px;
      margin-left:0; }
    .bp3-tag-input.bp3-large .bp3-spinner{
      margin:8px;
      margin-left:0; }
  .bp3-tag-input.bp3-active{
    background-color:#ffffff;
    -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-tag-input.bp3-active.bp3-intent-primary{
      -webkit-box-shadow:0 0 0 1px #106ba3, 0 0 0 3px rgba(16, 107, 163, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #106ba3, 0 0 0 3px rgba(16, 107, 163, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-tag-input.bp3-active.bp3-intent-success{
      -webkit-box-shadow:0 0 0 1px #0d8050, 0 0 0 3px rgba(13, 128, 80, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #0d8050, 0 0 0 3px rgba(13, 128, 80, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-tag-input.bp3-active.bp3-intent-warning{
      -webkit-box-shadow:0 0 0 1px #bf7326, 0 0 0 3px rgba(191, 115, 38, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #bf7326, 0 0 0 3px rgba(191, 115, 38, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-tag-input.bp3-active.bp3-intent-danger{
      -webkit-box-shadow:0 0 0 1px #c23030, 0 0 0 3px rgba(194, 48, 48, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #c23030, 0 0 0 3px rgba(194, 48, 48, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-dark .bp3-tag-input .bp3-tag-input-icon, .bp3-tag-input.bp3-dark .bp3-tag-input-icon{
    color:#a7b6c2; }
  .bp3-dark .bp3-tag-input .bp3-input-ghost, .bp3-tag-input.bp3-dark .bp3-input-ghost{
    color:#f5f8fa; }
    .bp3-dark .bp3-tag-input .bp3-input-ghost::-webkit-input-placeholder, .bp3-tag-input.bp3-dark .bp3-input-ghost::-webkit-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-tag-input .bp3-input-ghost::-moz-placeholder, .bp3-tag-input.bp3-dark .bp3-input-ghost::-moz-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-tag-input .bp3-input-ghost:-ms-input-placeholder, .bp3-tag-input.bp3-dark .bp3-input-ghost:-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-tag-input .bp3-input-ghost::-ms-input-placeholder, .bp3-tag-input.bp3-dark .bp3-input-ghost::-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-tag-input .bp3-input-ghost::placeholder, .bp3-tag-input.bp3-dark .bp3-input-ghost::placeholder{
      color:rgba(167, 182, 194, 0.6); }
  .bp3-dark .bp3-tag-input.bp3-active, .bp3-tag-input.bp3-dark.bp3-active{
    background-color:rgba(16, 22, 26, 0.3);
    -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-tag-input.bp3-active.bp3-intent-primary, .bp3-tag-input.bp3-dark.bp3-active.bp3-intent-primary{
      -webkit-box-shadow:0 0 0 1px #106ba3, 0 0 0 3px rgba(16, 107, 163, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px #106ba3, 0 0 0 3px rgba(16, 107, 163, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-tag-input.bp3-active.bp3-intent-success, .bp3-tag-input.bp3-dark.bp3-active.bp3-intent-success{
      -webkit-box-shadow:0 0 0 1px #0d8050, 0 0 0 3px rgba(13, 128, 80, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px #0d8050, 0 0 0 3px rgba(13, 128, 80, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-tag-input.bp3-active.bp3-intent-warning, .bp3-tag-input.bp3-dark.bp3-active.bp3-intent-warning{
      -webkit-box-shadow:0 0 0 1px #bf7326, 0 0 0 3px rgba(191, 115, 38, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px #bf7326, 0 0 0 3px rgba(191, 115, 38, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-tag-input.bp3-active.bp3-intent-danger, .bp3-tag-input.bp3-dark.bp3-active.bp3-intent-danger{
      -webkit-box-shadow:0 0 0 1px #c23030, 0 0 0 3px rgba(194, 48, 48, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px #c23030, 0 0 0 3px rgba(194, 48, 48, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }

.bp3-input-ghost{
  background:none;
  border:none;
  -webkit-box-shadow:none;
          box-shadow:none;
  padding:0; }
  .bp3-input-ghost::-webkit-input-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-input-ghost::-moz-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-input-ghost:-ms-input-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-input-ghost::-ms-input-placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-input-ghost::placeholder{
    color:rgba(92, 112, 128, 0.6);
    opacity:1; }
  .bp3-input-ghost:focus{
    outline:none !important; }
.bp3-toast{
  -webkit-box-align:start;
      -ms-flex-align:start;
          align-items:flex-start;
  background-color:#ffffff;
  border-radius:3px;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  margin:20px 0 0;
  max-width:500px;
  min-width:300px;
  pointer-events:all;
  position:relative !important; }
  .bp3-toast.bp3-toast-enter, .bp3-toast.bp3-toast-appear{
    -webkit-transform:translateY(-40px);
            transform:translateY(-40px); }
  .bp3-toast.bp3-toast-enter-active, .bp3-toast.bp3-toast-appear-active{
    -webkit-transform:translateY(0);
            transform:translateY(0);
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:300ms;
            transition-duration:300ms;
    -webkit-transition-property:-webkit-transform;
    transition-property:-webkit-transform;
    transition-property:transform;
    transition-property:transform, -webkit-transform;
    -webkit-transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
            transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11); }
  .bp3-toast.bp3-toast-enter ~ .bp3-toast, .bp3-toast.bp3-toast-appear ~ .bp3-toast{
    -webkit-transform:translateY(-40px);
            transform:translateY(-40px); }
  .bp3-toast.bp3-toast-enter-active ~ .bp3-toast, .bp3-toast.bp3-toast-appear-active ~ .bp3-toast{
    -webkit-transform:translateY(0);
            transform:translateY(0);
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:300ms;
            transition-duration:300ms;
    -webkit-transition-property:-webkit-transform;
    transition-property:-webkit-transform;
    transition-property:transform;
    transition-property:transform, -webkit-transform;
    -webkit-transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
            transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11); }
  .bp3-toast.bp3-toast-exit{
    opacity:1;
    -webkit-filter:blur(0);
            filter:blur(0); }
  .bp3-toast.bp3-toast-exit-active{
    opacity:0;
    -webkit-filter:blur(10px);
            filter:blur(10px);
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:300ms;
            transition-duration:300ms;
    -webkit-transition-property:opacity, -webkit-filter;
    transition-property:opacity, -webkit-filter;
    transition-property:opacity, filter;
    transition-property:opacity, filter, -webkit-filter;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-toast.bp3-toast-exit ~ .bp3-toast{
    -webkit-transform:translateY(0);
            transform:translateY(0); }
  .bp3-toast.bp3-toast-exit-active ~ .bp3-toast{
    -webkit-transform:translateY(-40px);
            transform:translateY(-40px);
    -webkit-transition-delay:50ms;
            transition-delay:50ms;
    -webkit-transition-duration:100ms;
            transition-duration:100ms;
    -webkit-transition-property:-webkit-transform;
    transition-property:-webkit-transform;
    transition-property:transform;
    transition-property:transform, -webkit-transform;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-toast .bp3-button-group{
    -webkit-box-flex:0;
        -ms-flex:0 0 auto;
            flex:0 0 auto;
    padding:5px;
    padding-left:0; }
  .bp3-toast > .bp3-icon{
    color:#5c7080;
    margin:12px;
    margin-right:0; }
  .bp3-toast.bp3-dark,
  .bp3-dark .bp3-toast{
    background-color:#394b59;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4); }
    .bp3-toast.bp3-dark > .bp3-icon,
    .bp3-dark .bp3-toast > .bp3-icon{
      color:#a7b6c2; }
  .bp3-toast[class*="bp3-intent-"] a{
    color:rgba(255, 255, 255, 0.7); }
    .bp3-toast[class*="bp3-intent-"] a:hover{
      color:#ffffff; }
  .bp3-toast[class*="bp3-intent-"] > .bp3-icon{
    color:#ffffff; }
  .bp3-toast[class*="bp3-intent-"] .bp3-button, .bp3-toast[class*="bp3-intent-"] .bp3-button::before,
  .bp3-toast[class*="bp3-intent-"] .bp3-button .bp3-icon, .bp3-toast[class*="bp3-intent-"] .bp3-button:active{
    color:rgba(255, 255, 255, 0.7) !important; }
  .bp3-toast[class*="bp3-intent-"] .bp3-button:focus{
    outline-color:rgba(255, 255, 255, 0.5); }
  .bp3-toast[class*="bp3-intent-"] .bp3-button:hover{
    background-color:rgba(255, 255, 255, 0.15) !important;
    color:#ffffff !important; }
  .bp3-toast[class*="bp3-intent-"] .bp3-button:active{
    background-color:rgba(255, 255, 255, 0.3) !important;
    color:#ffffff !important; }
  .bp3-toast[class*="bp3-intent-"] .bp3-button::after{
    background:rgba(255, 255, 255, 0.3) !important; }
  .bp3-toast.bp3-intent-primary{
    background-color:#137cbd;
    color:#ffffff; }
  .bp3-toast.bp3-intent-success{
    background-color:#0f9960;
    color:#ffffff; }
  .bp3-toast.bp3-intent-warning{
    background-color:#d9822b;
    color:#ffffff; }
  .bp3-toast.bp3-intent-danger{
    background-color:#db3737;
    color:#ffffff; }

.bp3-toast-message{
  -webkit-box-flex:1;
      -ms-flex:1 1 auto;
          flex:1 1 auto;
  padding:11px;
  word-break:break-word; }

.bp3-toast-container{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  display:-webkit-box !important;
  display:-ms-flexbox !important;
  display:flex !important;
  -webkit-box-orient:vertical;
  -webkit-box-direction:normal;
      -ms-flex-direction:column;
          flex-direction:column;
  left:0;
  overflow:hidden;
  padding:0 20px 20px;
  pointer-events:none;
  right:0;
  z-index:40; }
  .bp3-toast-container.bp3-toast-container-in-portal{
    position:fixed; }
  .bp3-toast-container.bp3-toast-container-inline{
    position:absolute; }
  .bp3-toast-container.bp3-toast-container-top{
    top:0; }
  .bp3-toast-container.bp3-toast-container-bottom{
    bottom:0;
    -webkit-box-orient:vertical;
    -webkit-box-direction:reverse;
        -ms-flex-direction:column-reverse;
            flex-direction:column-reverse;
    top:auto; }
  .bp3-toast-container.bp3-toast-container-left{
    -webkit-box-align:start;
        -ms-flex-align:start;
            align-items:flex-start; }
  .bp3-toast-container.bp3-toast-container-right{
    -webkit-box-align:end;
        -ms-flex-align:end;
            align-items:flex-end; }

.bp3-toast-container-bottom .bp3-toast.bp3-toast-enter:not(.bp3-toast-enter-active),
.bp3-toast-container-bottom .bp3-toast.bp3-toast-enter:not(.bp3-toast-enter-active) ~ .bp3-toast, .bp3-toast-container-bottom .bp3-toast.bp3-toast-appear:not(.bp3-toast-appear-active),
.bp3-toast-container-bottom .bp3-toast.bp3-toast-appear:not(.bp3-toast-appear-active) ~ .bp3-toast,
.bp3-toast-container-bottom .bp3-toast.bp3-toast-exit-active ~ .bp3-toast,
.bp3-toast-container-bottom .bp3-toast.bp3-toast-leave-active ~ .bp3-toast{
  -webkit-transform:translateY(60px);
          transform:translateY(60px); }
.bp3-tooltip{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
  -webkit-transform:scale(1);
          transform:scale(1); }
  .bp3-tooltip .bp3-popover-arrow{
    height:22px;
    position:absolute;
    width:22px; }
    .bp3-tooltip .bp3-popover-arrow::before{
      height:14px;
      margin:4px;
      width:14px; }
  .bp3-tether-element-attached-bottom.bp3-tether-target-attached-top > .bp3-tooltip{
    margin-bottom:11px;
    margin-top:-11px; }
    .bp3-tether-element-attached-bottom.bp3-tether-target-attached-top > .bp3-tooltip > .bp3-popover-arrow{
      bottom:-8px; }
      .bp3-tether-element-attached-bottom.bp3-tether-target-attached-top > .bp3-tooltip > .bp3-popover-arrow svg{
        -webkit-transform:rotate(-90deg);
                transform:rotate(-90deg); }
  .bp3-tether-element-attached-left.bp3-tether-target-attached-right > .bp3-tooltip{
    margin-left:11px; }
    .bp3-tether-element-attached-left.bp3-tether-target-attached-right > .bp3-tooltip > .bp3-popover-arrow{
      left:-8px; }
      .bp3-tether-element-attached-left.bp3-tether-target-attached-right > .bp3-tooltip > .bp3-popover-arrow svg{
        -webkit-transform:rotate(0);
                transform:rotate(0); }
  .bp3-tether-element-attached-top.bp3-tether-target-attached-bottom > .bp3-tooltip{
    margin-top:11px; }
    .bp3-tether-element-attached-top.bp3-tether-target-attached-bottom > .bp3-tooltip > .bp3-popover-arrow{
      top:-8px; }
      .bp3-tether-element-attached-top.bp3-tether-target-attached-bottom > .bp3-tooltip > .bp3-popover-arrow svg{
        -webkit-transform:rotate(90deg);
                transform:rotate(90deg); }
  .bp3-tether-element-attached-right.bp3-tether-target-attached-left > .bp3-tooltip{
    margin-left:-11px;
    margin-right:11px; }
    .bp3-tether-element-attached-right.bp3-tether-target-attached-left > .bp3-tooltip > .bp3-popover-arrow{
      right:-8px; }
      .bp3-tether-element-attached-right.bp3-tether-target-attached-left > .bp3-tooltip > .bp3-popover-arrow svg{
        -webkit-transform:rotate(180deg);
                transform:rotate(180deg); }
  .bp3-tether-element-attached-middle > .bp3-tooltip > .bp3-popover-arrow{
    top:50%;
    -webkit-transform:translateY(-50%);
            transform:translateY(-50%); }
  .bp3-tether-element-attached-center > .bp3-tooltip > .bp3-popover-arrow{
    right:50%;
    -webkit-transform:translateX(50%);
            transform:translateX(50%); }
  .bp3-tether-element-attached-top.bp3-tether-target-attached-top > .bp3-tooltip > .bp3-popover-arrow{
    top:-0.22183px; }
  .bp3-tether-element-attached-right.bp3-tether-target-attached-right > .bp3-tooltip > .bp3-popover-arrow{
    right:-0.22183px; }
  .bp3-tether-element-attached-left.bp3-tether-target-attached-left > .bp3-tooltip > .bp3-popover-arrow{
    left:-0.22183px; }
  .bp3-tether-element-attached-bottom.bp3-tether-target-attached-bottom > .bp3-tooltip > .bp3-popover-arrow{
    bottom:-0.22183px; }
  .bp3-tether-element-attached-top.bp3-tether-element-attached-left > .bp3-tooltip{
    -webkit-transform-origin:top left;
            transform-origin:top left; }
  .bp3-tether-element-attached-top.bp3-tether-element-attached-center > .bp3-tooltip{
    -webkit-transform-origin:top center;
            transform-origin:top center; }
  .bp3-tether-element-attached-top.bp3-tether-element-attached-right > .bp3-tooltip{
    -webkit-transform-origin:top right;
            transform-origin:top right; }
  .bp3-tether-element-attached-middle.bp3-tether-element-attached-left > .bp3-tooltip{
    -webkit-transform-origin:center left;
            transform-origin:center left; }
  .bp3-tether-element-attached-middle.bp3-tether-element-attached-center > .bp3-tooltip{
    -webkit-transform-origin:center center;
            transform-origin:center center; }
  .bp3-tether-element-attached-middle.bp3-tether-element-attached-right > .bp3-tooltip{
    -webkit-transform-origin:center right;
            transform-origin:center right; }
  .bp3-tether-element-attached-bottom.bp3-tether-element-attached-left > .bp3-tooltip{
    -webkit-transform-origin:bottom left;
            transform-origin:bottom left; }
  .bp3-tether-element-attached-bottom.bp3-tether-element-attached-center > .bp3-tooltip{
    -webkit-transform-origin:bottom center;
            transform-origin:bottom center; }
  .bp3-tether-element-attached-bottom.bp3-tether-element-attached-right > .bp3-tooltip{
    -webkit-transform-origin:bottom right;
            transform-origin:bottom right; }
  .bp3-tooltip .bp3-popover-content{
    background:#394b59;
    color:#f5f8fa; }
  .bp3-tooltip .bp3-popover-arrow::before{
    -webkit-box-shadow:1px 1px 6px rgba(16, 22, 26, 0.2);
            box-shadow:1px 1px 6px rgba(16, 22, 26, 0.2); }
  .bp3-tooltip .bp3-popover-arrow-border{
    fill:#10161a;
    fill-opacity:0.1; }
  .bp3-tooltip .bp3-popover-arrow-fill{
    fill:#394b59; }
  .bp3-popover-enter > .bp3-tooltip, .bp3-popover-appear > .bp3-tooltip{
    -webkit-transform:scale(0.8);
            transform:scale(0.8); }
  .bp3-popover-enter-active > .bp3-tooltip, .bp3-popover-appear-active > .bp3-tooltip{
    -webkit-transform:scale(1);
            transform:scale(1);
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:100ms;
            transition-duration:100ms;
    -webkit-transition-property:-webkit-transform;
    transition-property:-webkit-transform;
    transition-property:transform;
    transition-property:transform, -webkit-transform;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-popover-exit > .bp3-tooltip{
    -webkit-transform:scale(1);
            transform:scale(1); }
  .bp3-popover-exit-active > .bp3-tooltip{
    -webkit-transform:scale(0.8);
            transform:scale(0.8);
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:100ms;
            transition-duration:100ms;
    -webkit-transition-property:-webkit-transform;
    transition-property:-webkit-transform;
    transition-property:transform;
    transition-property:transform, -webkit-transform;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-tooltip .bp3-popover-content{
    padding:10px 12px; }
  .bp3-tooltip.bp3-dark,
  .bp3-dark .bp3-tooltip{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4); }
    .bp3-tooltip.bp3-dark .bp3-popover-content,
    .bp3-dark .bp3-tooltip .bp3-popover-content{
      background:#e1e8ed;
      color:#394b59; }
    .bp3-tooltip.bp3-dark .bp3-popover-arrow::before,
    .bp3-dark .bp3-tooltip .bp3-popover-arrow::before{
      -webkit-box-shadow:1px 1px 6px rgba(16, 22, 26, 0.4);
              box-shadow:1px 1px 6px rgba(16, 22, 26, 0.4); }
    .bp3-tooltip.bp3-dark .bp3-popover-arrow-border,
    .bp3-dark .bp3-tooltip .bp3-popover-arrow-border{
      fill:#10161a;
      fill-opacity:0.2; }
    .bp3-tooltip.bp3-dark .bp3-popover-arrow-fill,
    .bp3-dark .bp3-tooltip .bp3-popover-arrow-fill{
      fill:#e1e8ed; }
  .bp3-tooltip.bp3-intent-primary .bp3-popover-content{
    background:#137cbd;
    color:#ffffff; }
  .bp3-tooltip.bp3-intent-primary .bp3-popover-arrow-fill{
    fill:#137cbd; }
  .bp3-tooltip.bp3-intent-success .bp3-popover-content{
    background:#0f9960;
    color:#ffffff; }
  .bp3-tooltip.bp3-intent-success .bp3-popover-arrow-fill{
    fill:#0f9960; }
  .bp3-tooltip.bp3-intent-warning .bp3-popover-content{
    background:#d9822b;
    color:#ffffff; }
  .bp3-tooltip.bp3-intent-warning .bp3-popover-arrow-fill{
    fill:#d9822b; }
  .bp3-tooltip.bp3-intent-danger .bp3-popover-content{
    background:#db3737;
    color:#ffffff; }
  .bp3-tooltip.bp3-intent-danger .bp3-popover-arrow-fill{
    fill:#db3737; }

.bp3-tooltip-indicator{
  border-bottom:dotted 1px;
  cursor:help; }
.bp3-tree .bp3-icon, .bp3-tree .bp3-icon-standard, .bp3-tree .bp3-icon-large{
  color:#5c7080; }
  .bp3-tree .bp3-icon.bp3-intent-primary, .bp3-tree .bp3-icon-standard.bp3-intent-primary, .bp3-tree .bp3-icon-large.bp3-intent-primary{
    color:#137cbd; }
  .bp3-tree .bp3-icon.bp3-intent-success, .bp3-tree .bp3-icon-standard.bp3-intent-success, .bp3-tree .bp3-icon-large.bp3-intent-success{
    color:#0f9960; }
  .bp3-tree .bp3-icon.bp3-intent-warning, .bp3-tree .bp3-icon-standard.bp3-intent-warning, .bp3-tree .bp3-icon-large.bp3-intent-warning{
    color:#d9822b; }
  .bp3-tree .bp3-icon.bp3-intent-danger, .bp3-tree .bp3-icon-standard.bp3-intent-danger, .bp3-tree .bp3-icon-large.bp3-intent-danger{
    color:#db3737; }

.bp3-tree-node-list{
  list-style:none;
  margin:0;
  padding-left:0; }

.bp3-tree-root{
  background-color:transparent;
  cursor:default;
  padding-left:0;
  position:relative; }

.bp3-tree-node-content-0{
  padding-left:0px; }

.bp3-tree-node-content-1{
  padding-left:23px; }

.bp3-tree-node-content-2{
  padding-left:46px; }

.bp3-tree-node-content-3{
  padding-left:69px; }

.bp3-tree-node-content-4{
  padding-left:92px; }

.bp3-tree-node-content-5{
  padding-left:115px; }

.bp3-tree-node-content-6{
  padding-left:138px; }

.bp3-tree-node-content-7{
  padding-left:161px; }

.bp3-tree-node-content-8{
  padding-left:184px; }

.bp3-tree-node-content-9{
  padding-left:207px; }

.bp3-tree-node-content-10{
  padding-left:230px; }

.bp3-tree-node-content-11{
  padding-left:253px; }

.bp3-tree-node-content-12{
  padding-left:276px; }

.bp3-tree-node-content-13{
  padding-left:299px; }

.bp3-tree-node-content-14{
  padding-left:322px; }

.bp3-tree-node-content-15{
  padding-left:345px; }

.bp3-tree-node-content-16{
  padding-left:368px; }

.bp3-tree-node-content-17{
  padding-left:391px; }

.bp3-tree-node-content-18{
  padding-left:414px; }

.bp3-tree-node-content-19{
  padding-left:437px; }

.bp3-tree-node-content-20{
  padding-left:460px; }

.bp3-tree-node-content{
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  height:30px;
  padding-right:5px;
  width:100%; }
  .bp3-tree-node-content:hover{
    background-color:rgba(191, 204, 214, 0.4); }

.bp3-tree-node-caret,
.bp3-tree-node-caret-none{
  min-width:30px; }

.bp3-tree-node-caret{
  color:#5c7080;
  cursor:pointer;
  padding:7px;
  -webkit-transform:rotate(0deg);
          transform:rotate(0deg);
  -webkit-transition:-webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:-webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-tree-node-caret:hover{
    color:#182026; }
  .bp3-dark .bp3-tree-node-caret{
    color:#a7b6c2; }
    .bp3-dark .bp3-tree-node-caret:hover{
      color:#f5f8fa; }
  .bp3-tree-node-caret.bp3-tree-node-caret-open{
    -webkit-transform:rotate(90deg);
            transform:rotate(90deg); }
  .bp3-tree-node-caret.bp3-icon-standard::before{
    content:""; }

.bp3-tree-node-icon{
  margin-right:7px;
  position:relative; }

.bp3-tree-node-label{
  overflow:hidden;
  text-overflow:ellipsis;
  white-space:nowrap;
  word-wrap:normal;
  -webkit-box-flex:1;
      -ms-flex:1 1 auto;
          flex:1 1 auto;
  position:relative;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none; }
  .bp3-tree-node-label span{
    display:inline; }

.bp3-tree-node-secondary-label{
  padding:0 5px;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none; }
  .bp3-tree-node-secondary-label .bp3-popover-wrapper,
  .bp3-tree-node-secondary-label .bp3-popover-target{
    -webkit-box-align:center;
        -ms-flex-align:center;
            align-items:center;
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex; }

.bp3-tree-node.bp3-disabled .bp3-tree-node-content{
  background-color:inherit;
  color:rgba(92, 112, 128, 0.6);
  cursor:not-allowed; }

.bp3-tree-node.bp3-disabled .bp3-tree-node-caret,
.bp3-tree-node.bp3-disabled .bp3-tree-node-icon{
  color:rgba(92, 112, 128, 0.6);
  cursor:not-allowed; }

.bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content{
  background-color:#137cbd; }
  .bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content,
  .bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content .bp3-icon, .bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content .bp3-icon-standard, .bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content .bp3-icon-large{
    color:#ffffff; }
  .bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content .bp3-tree-node-caret::before{
    color:rgba(255, 255, 255, 0.7); }
  .bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content .bp3-tree-node-caret:hover::before{
    color:#ffffff; }

.bp3-dark .bp3-tree-node-content:hover{
  background-color:rgba(92, 112, 128, 0.3); }

.bp3-dark .bp3-tree .bp3-icon, .bp3-dark .bp3-tree .bp3-icon-standard, .bp3-dark .bp3-tree .bp3-icon-large{
  color:#a7b6c2; }
  .bp3-dark .bp3-tree .bp3-icon.bp3-intent-primary, .bp3-dark .bp3-tree .bp3-icon-standard.bp3-intent-primary, .bp3-dark .bp3-tree .bp3-icon-large.bp3-intent-primary{
    color:#137cbd; }
  .bp3-dark .bp3-tree .bp3-icon.bp3-intent-success, .bp3-dark .bp3-tree .bp3-icon-standard.bp3-intent-success, .bp3-dark .bp3-tree .bp3-icon-large.bp3-intent-success{
    color:#0f9960; }
  .bp3-dark .bp3-tree .bp3-icon.bp3-intent-warning, .bp3-dark .bp3-tree .bp3-icon-standard.bp3-intent-warning, .bp3-dark .bp3-tree .bp3-icon-large.bp3-intent-warning{
    color:#d9822b; }
  .bp3-dark .bp3-tree .bp3-icon.bp3-intent-danger, .bp3-dark .bp3-tree .bp3-icon-standard.bp3-intent-danger, .bp3-dark .bp3-tree .bp3-icon-large.bp3-intent-danger{
    color:#db3737; }

.bp3-dark .bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content{
  background-color:#137cbd; }
.bp3-omnibar{
  -webkit-filter:blur(0);
          filter:blur(0);
  opacity:1;
  background-color:#ffffff;
  border-radius:3px;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2);
  left:calc(50% - 250px);
  top:20vh;
  width:500px;
  z-index:21; }
  .bp3-omnibar.bp3-overlay-enter, .bp3-omnibar.bp3-overlay-appear{
    -webkit-filter:blur(20px);
            filter:blur(20px);
    opacity:0.2; }
  .bp3-omnibar.bp3-overlay-enter-active, .bp3-omnibar.bp3-overlay-appear-active{
    -webkit-filter:blur(0);
            filter:blur(0);
    opacity:1;
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:200ms;
            transition-duration:200ms;
    -webkit-transition-property:opacity, -webkit-filter;
    transition-property:opacity, -webkit-filter;
    transition-property:filter, opacity;
    transition-property:filter, opacity, -webkit-filter;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-omnibar.bp3-overlay-exit{
    -webkit-filter:blur(0);
            filter:blur(0);
    opacity:1; }
  .bp3-omnibar.bp3-overlay-exit-active{
    -webkit-filter:blur(20px);
            filter:blur(20px);
    opacity:0.2;
    -webkit-transition-delay:0;
            transition-delay:0;
    -webkit-transition-duration:200ms;
            transition-duration:200ms;
    -webkit-transition-property:opacity, -webkit-filter;
    transition-property:opacity, -webkit-filter;
    transition-property:filter, opacity;
    transition-property:filter, opacity, -webkit-filter;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-omnibar .bp3-input{
    background-color:transparent;
    border-radius:0; }
    .bp3-omnibar .bp3-input, .bp3-omnibar .bp3-input:focus{
      -webkit-box-shadow:none;
              box-shadow:none; }
  .bp3-omnibar .bp3-menu{
    background-color:transparent;
    border-radius:0;
    -webkit-box-shadow:inset 0 1px 0 rgba(16, 22, 26, 0.15);
            box-shadow:inset 0 1px 0 rgba(16, 22, 26, 0.15);
    max-height:calc(60vh - 40px);
    overflow:auto; }
    .bp3-omnibar .bp3-menu:empty{
      display:none; }
  .bp3-dark .bp3-omnibar, .bp3-omnibar.bp3-dark{
    background-color:#30404d;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4); }

.bp3-omnibar-overlay .bp3-overlay-backdrop{
  background-color:rgba(16, 22, 26, 0.2); }

.bp3-select-popover .bp3-popover-content{
  padding:5px; }

.bp3-select-popover .bp3-input-group{
  margin-bottom:0; }

.bp3-select-popover .bp3-menu{
  max-height:300px;
  max-width:400px;
  overflow:auto;
  padding:0; }
  .bp3-select-popover .bp3-menu:not(:first-child){
    padding-top:5px; }

.bp3-multi-select{
  min-width:150px; }

.bp3-multi-select-popover .bp3-menu{
  max-height:300px;
  max-width:400px;
  overflow:auto; }

.bp3-select-popover .bp3-popover-content{
  padding:5px; }

.bp3-select-popover .bp3-input-group{
  margin-bottom:0; }

.bp3-select-popover .bp3-menu{
  max-height:300px;
  max-width:400px;
  overflow:auto;
  padding:0; }
  .bp3-select-popover .bp3-menu:not(:first-child){
    padding-top:5px; }
/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/* This file was auto-generated by ensureUiComponents() in @jupyterlab/buildutils */

/**
 * (DEPRECATED) Support for consuming icons as CSS background images
 */

/* Icons urls */

:root {
  --jp-icon-add: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTE5IDEzaC02djZoLTJ2LTZINXYtMmg2VjVoMnY2aDZ2MnoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-bug: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIj4KICAgIDxwYXRoIGQ9Ik0yMCA4aC0yLjgxYy0uNDUtLjc4LTEuMDctMS40NS0xLjgyLTEuOTZMMTcgNC40MSAxNS41OSAzbC0yLjE3IDIuMTdDMTIuOTYgNS4wNiAxMi40OSA1IDEyIDVjLS40OSAwLS45Ni4wNi0xLjQxLjE3TDguNDEgMyA3IDQuNDFsMS42MiAxLjYzQzcuODggNi41NSA3LjI2IDcuMjIgNi44MSA4SDR2MmgyLjA5Yy0uMDUuMzMtLjA5LjY2LS4wOSAxdjFINHYyaDJ2MWMwIC4zNC4wNC42Ny4wOSAxSDR2MmgyLjgxYzEuMDQgMS43OSAyLjk3IDMgNS4xOSAzczQuMTUtMS4yMSA1LjE5LTNIMjB2LTJoLTIuMDljLjA1LS4zMy4wOS0uNjYuMDktMXYtMWgydi0yaC0ydi0xYzAtLjM0LS4wNC0uNjctLjA5LTFIMjBWOHptLTYgOGgtNHYtMmg0djJ6bTAtNGgtNHYtMmg0djJ6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-build: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTYiIHZpZXdCb3g9IjAgMCAyNCAyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTE0LjkgMTcuNDVDMTYuMjUgMTcuNDUgMTcuMzUgMTYuMzUgMTcuMzUgMTVDMTcuMzUgMTMuNjUgMTYuMjUgMTIuNTUgMTQuOSAxMi41NUMxMy41NCAxMi41NSAxMi40NSAxMy42NSAxMi40NSAxNUMxMi40NSAxNi4zNSAxMy41NCAxNy40NSAxNC45IDE3LjQ1Wk0yMC4xIDE1LjY4TDIxLjU4IDE2Ljg0QzIxLjcxIDE2Ljk1IDIxLjc1IDE3LjEzIDIxLjY2IDE3LjI5TDIwLjI2IDE5LjcxQzIwLjE3IDE5Ljg2IDIwIDE5LjkyIDE5LjgzIDE5Ljg2TDE4LjA5IDE5LjE2QzE3LjczIDE5LjQ0IDE3LjMzIDE5LjY3IDE2LjkxIDE5Ljg1TDE2LjY0IDIxLjdDMTYuNjIgMjEuODcgMTYuNDcgMjIgMTYuMyAyMkgxMy41QzEzLjMyIDIyIDEzLjE4IDIxLjg3IDEzLjE1IDIxLjdMMTIuODkgMTkuODVDMTIuNDYgMTkuNjcgMTIuMDcgMTkuNDQgMTEuNzEgMTkuMTZMOS45NjAwMiAxOS44NkM5LjgxMDAyIDE5LjkyIDkuNjIwMDIgMTkuODYgOS41NDAwMiAxOS43MUw4LjE0MDAyIDE3LjI5QzguMDUwMDIgMTcuMTMgOC4wOTAwMiAxNi45NSA4LjIyMDAyIDE2Ljg0TDkuNzAwMDIgMTUuNjhMOS42NTAwMSAxNUw5LjcwMDAyIDE0LjMxTDguMjIwMDIgMTMuMTZDOC4wOTAwMiAxMy4wNSA4LjA1MDAyIDEyLjg2IDguMTQwMDIgMTIuNzFMOS41NDAwMiAxMC4yOUM5LjYyMDAyIDEwLjEzIDkuODEwMDIgMTAuMDcgOS45NjAwMiAxMC4xM0wxMS43MSAxMC44NEMxMi4wNyAxMC41NiAxMi40NiAxMC4zMiAxMi44OSAxMC4xNUwxMy4xNSA4LjI4OTk4QzEzLjE4IDguMTI5OTggMTMuMzIgNy45OTk5OCAxMy41IDcuOTk5OThIMTYuM0MxNi40NyA3Ljk5OTk4IDE2LjYyIDguMTI5OTggMTYuNjQgOC4yODk5OEwxNi45MSAxMC4xNUMxNy4zMyAxMC4zMiAxNy43MyAxMC41NiAxOC4wOSAxMC44NEwxOS44MyAxMC4xM0MyMCAxMC4wNyAyMC4xNyAxMC4xMyAyMC4yNiAxMC4yOUwyMS42NiAxMi43MUMyMS43NSAxMi44NiAyMS43MSAxMy4wNSAyMS41OCAxMy4xNkwyMC4xIDE0LjMxTDIwLjE1IDE1TDIwLjEgMTUuNjhaIi8+CiAgICA8cGF0aCBkPSJNNy4zMjk2NiA3LjQ0NDU0QzguMDgzMSA3LjAwOTU0IDguMzM5MzIgNi4wNTMzMiA3LjkwNDMyIDUuMjk5ODhDNy40NjkzMiA0LjU0NjQzIDYuNTA4MSA0LjI4MTU2IDUuNzU0NjYgNC43MTY1NkM1LjM5MTc2IDQuOTI2MDggNS4xMjY5NSA1LjI3MTE4IDUuMDE4NDkgNS42NzU5NEM0LjkxMDA0IDYuMDgwNzEgNC45NjY4MiA2LjUxMTk4IDUuMTc2MzQgNi44NzQ4OEM1LjYxMTM0IDcuNjI4MzIgNi41NzYyMiA3Ljg3OTU0IDcuMzI5NjYgNy40NDQ1NFpNOS42NTcxOCA0Ljc5NTkzTDEwLjg2NzIgNC45NTE3OUMxMC45NjI4IDQuOTc3NDEgMTEuMDQwMiA1LjA3MTMzIDExLjAzODIgNS4xODc5M0wxMS4wMzg4IDYuOTg4OTNDMTEuMDQ1NSA3LjEwMDU0IDEwLjk2MTYgNy4xOTUxOCAxMC44NTUgNy4yMTA1NEw5LjY2MDAxIDcuMzgwODNMOS4yMzkxNSA4LjEzMTg4TDkuNjY5NjEgOS4yNTc0NUM5LjcwNzI5IDkuMzYyNzEgOS42NjkzNCA5LjQ3Njk5IDkuNTc0MDggOS41MzE5OUw4LjAxNTIzIDEwLjQzMkM3LjkxMTMxIDEwLjQ5MiA3Ljc5MzM3IDEwLjQ2NzcgNy43MjEwNSAxMC4zODI0TDYuOTg3NDggOS40MzE4OEw2LjEwOTMxIDkuNDMwODNMNS4zNDcwNCAxMC4zOTA1QzUuMjg5MDkgMTAuNDcwMiA1LjE3MzgzIDEwLjQ5MDUgNS4wNzE4NyAxMC40MzM5TDMuNTEyNDUgOS41MzI5M0MzLjQxMDQ5IDkuNDc2MzMgMy4zNzY0NyA5LjM1NzQxIDMuNDEwNzUgOS4yNTY3OUwzLjg2MzQ3IDguMTQwOTNMMy42MTc0OSA3Ljc3NDg4TDMuNDIzNDcgNy4zNzg4M0wyLjIzMDc1IDcuMjEyOTdDMi4xMjY0NyA3LjE5MjM1IDIuMDQwNDkgNy4xMDM0MiAyLjA0MjQ1IDYuOTg2ODJMMi4wNDE4NyA1LjE4NTgyQzIuMDQzODMgNS4wNjkyMiAyLjExOTA5IDQuOTc5NTggMi4yMTcwNCA0Ljk2OTIyTDMuNDIwNjUgNC43OTM5M0wzLjg2NzQ5IDQuMDI3ODhMMy40MTEwNSAyLjkxNzMxQzMuMzczMzcgMi44MTIwNCAzLjQxMTMxIDIuNjk3NzYgMy41MTUyMyAyLjYzNzc2TDUuMDc0MDggMS43Mzc3NkM1LjE2OTM0IDEuNjgyNzYgNS4yODcyOSAxLjcwNzA0IDUuMzU5NjEgMS43OTIzMUw2LjExOTE1IDIuNzI3ODhMNi45ODAwMSAyLjczODkzTDcuNzI0OTYgMS43ODkyMkM3Ljc5MTU2IDEuNzA0NTggNy45MTU0OCAxLjY3OTIyIDguMDA4NzkgMS43NDA4Mkw5LjU2ODIxIDIuNjQxODJDOS42NzAxNyAyLjY5ODQyIDkuNzEyODUgMi44MTIzNCA5LjY4NzIzIDIuOTA3OTdMOS4yMTcxOCA0LjAzMzgzTDkuNDYzMTYgNC4zOTk4OEw5LjY1NzE4IDQuNzk1OTNaIi8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-caret-down-empty-thin: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIwIDIwIj4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSIgc2hhcGUtcmVuZGVyaW5nPSJnZW9tZXRyaWNQcmVjaXNpb24iPgoJCTxwb2x5Z29uIGNsYXNzPSJzdDEiIHBvaW50cz0iOS45LDEzLjYgMy42LDcuNCA0LjQsNi42IDkuOSwxMi4yIDE1LjQsNi43IDE2LjEsNy40ICIvPgoJPC9nPgo8L3N2Zz4K);
  --jp-icon-caret-down-empty: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiIHNoYXBlLXJlbmRlcmluZz0iZ2VvbWV0cmljUHJlY2lzaW9uIj4KICAgIDxwYXRoIGQ9Ik01LjIsNS45TDksOS43bDMuOC0zLjhsMS4yLDEuMmwtNC45LDVsLTQuOS01TDUuMiw1Ljl6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-caret-down: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiIHNoYXBlLXJlbmRlcmluZz0iZ2VvbWV0cmljUHJlY2lzaW9uIj4KICAgIDxwYXRoIGQ9Ik01LjIsNy41TDksMTEuMmwzLjgtMy44SDUuMnoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-caret-left: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSIgc2hhcGUtcmVuZGVyaW5nPSJnZW9tZXRyaWNQcmVjaXNpb24iPgoJCTxwYXRoIGQ9Ik0xMC44LDEyLjhMNy4xLDlsMy44LTMuOGwwLDcuNkgxMC44eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-caret-right: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiIHNoYXBlLXJlbmRlcmluZz0iZ2VvbWV0cmljUHJlY2lzaW9uIj4KICAgIDxwYXRoIGQ9Ik03LjIsNS4yTDEwLjksOWwtMy44LDMuOFY1LjJINy4yeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-caret-up-empty-thin: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIwIDIwIj4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSIgc2hhcGUtcmVuZGVyaW5nPSJnZW9tZXRyaWNQcmVjaXNpb24iPgoJCTxwb2x5Z29uIGNsYXNzPSJzdDEiIHBvaW50cz0iMTUuNCwxMy4zIDkuOSw3LjcgNC40LDEzLjIgMy42LDEyLjUgOS45LDYuMyAxNi4xLDEyLjYgIi8+Cgk8L2c+Cjwvc3ZnPgo=);
  --jp-icon-caret-up: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSIgc2hhcGUtcmVuZGVyaW5nPSJnZW9tZXRyaWNQcmVjaXNpb24iPgoJCTxwYXRoIGQ9Ik01LjIsMTAuNUw5LDYuOGwzLjgsMy44SDUuMnoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-case-sensitive: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIwIDIwIj4KICA8ZyBjbGFzcz0ianAtaWNvbjIiIGZpbGw9IiM0MTQxNDEiPgogICAgPHJlY3QgeD0iMiIgeT0iMiIgd2lkdGg9IjE2IiBoZWlnaHQ9IjE2Ii8+CiAgPC9nPgogIDxnIGNsYXNzPSJqcC1pY29uLWFjY2VudDIiIGZpbGw9IiNGRkYiPgogICAgPHBhdGggZD0iTTcuNiw4aDAuOWwzLjUsOGgtMS4xTDEwLDE0SDZsLTAuOSwySDRMNy42LDh6IE04LDkuMUw2LjQsMTNoMy4yTDgsOS4xeiIvPgogICAgPHBhdGggZD0iTTE2LjYsOS44Yy0wLjIsMC4xLTAuNCwwLjEtMC43LDAuMWMtMC4yLDAtMC40LTAuMS0wLjYtMC4yYy0wLjEtMC4xLTAuMi0wLjQtMC4yLTAuNyBjLTAuMywwLjMtMC42LDAuNS0wLjksMC43Yy0wLjMsMC4xLTAuNywwLjItMS4xLDAuMmMtMC4zLDAtMC41LDAtMC43LTAuMWMtMC4yLTAuMS0wLjQtMC4yLTAuNi0wLjNjLTAuMi0wLjEtMC4zLTAuMy0wLjQtMC41IGMtMC4xLTAuMi0wLjEtMC40LTAuMS0wLjdjMC0wLjMsMC4xLTAuNiwwLjItMC44YzAuMS0wLjIsMC4zLTAuNCwwLjQtMC41QzEyLDcsMTIuMiw2LjksMTIuNSw2LjhjMC4yLTAuMSwwLjUtMC4xLDAuNy0wLjIgYzAuMy0wLjEsMC41LTAuMSwwLjctMC4xYzAuMiwwLDAuNC0wLjEsMC42LTAuMWMwLjIsMCwwLjMtMC4xLDAuNC0wLjJjMC4xLTAuMSwwLjItMC4yLDAuMi0wLjRjMC0xLTEuMS0xLTEuMy0xIGMtMC40LDAtMS40LDAtMS40LDEuMmgtMC45YzAtMC40LDAuMS0wLjcsMC4yLTFjMC4xLTAuMiwwLjMtMC40LDAuNS0wLjZjMC4yLTAuMiwwLjUtMC4zLDAuOC0wLjNDMTMuMyw0LDEzLjYsNCwxMy45LDQgYzAuMywwLDAuNSwwLDAuOCwwLjFjMC4zLDAsMC41LDAuMSwwLjcsMC4yYzAuMiwwLjEsMC40LDAuMywwLjUsMC41QzE2LDUsMTYsNS4yLDE2LDUuNnYyLjljMCwwLjIsMCwwLjQsMCwwLjUgYzAsMC4xLDAuMSwwLjIsMC4zLDAuMmMwLjEsMCwwLjIsMCwwLjMsMFY5Ljh6IE0xNS4yLDYuOWMtMS4yLDAuNi0zLjEsMC4yLTMuMSwxLjRjMCwxLjQsMy4xLDEsMy4xLTAuNVY2Ljl6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-check: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIj4KICAgIDxwYXRoIGQ9Ik05IDE2LjE3TDQuODMgMTJsLTEuNDIgMS40MUw5IDE5IDIxIDdsLTEuNDEtMS40MXoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-circle-empty: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTEyIDJDNi40NyAyIDIgNi40NyAyIDEyczQuNDcgMTAgMTAgMTAgMTAtNC40NyAxMC0xMFMxNy41MyAyIDEyIDJ6bTAgMThjLTQuNDEgMC04LTMuNTktOC04czMuNTktOCA4LTggOCAzLjU5IDggOC0zLjU5IDgtOCA4eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-circle: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMTggMTgiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPGNpcmNsZSBjeD0iOSIgY3k9IjkiIHI9IjgiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-clear: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8bWFzayBpZD0iZG9udXRIb2xlIj4KICAgIDxyZWN0IHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgZmlsbD0id2hpdGUiIC8+CiAgICA8Y2lyY2xlIGN4PSIxMiIgY3k9IjEyIiByPSI4IiBmaWxsPSJibGFjayIvPgogIDwvbWFzaz4KCiAgPGcgY2xhc3M9ImpwLWljb24zIiBmaWxsPSIjNjE2MTYxIj4KICAgIDxyZWN0IGhlaWdodD0iMTgiIHdpZHRoPSIyIiB4PSIxMSIgeT0iMyIgdHJhbnNmb3JtPSJyb3RhdGUoMzE1LCAxMiwgMTIpIi8+CiAgICA8Y2lyY2xlIGN4PSIxMiIgY3k9IjEyIiByPSIxMCIgbWFzaz0idXJsKCNkb251dEhvbGUpIi8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-close: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbi1ub25lIGpwLWljb24tc2VsZWN0YWJsZS1pbnZlcnNlIGpwLWljb24zLWhvdmVyIiBmaWxsPSJub25lIj4KICAgIDxjaXJjbGUgY3g9IjEyIiBjeT0iMTIiIHI9IjExIi8+CiAgPC9nPgoKICA8ZyBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIGpwLWljb24tYWNjZW50Mi1ob3ZlciIgZmlsbD0iIzYxNjE2MSI+CiAgICA8cGF0aCBkPSJNMTkgNi40MUwxNy41OSA1IDEyIDEwLjU5IDYuNDEgNSA1IDYuNDEgMTAuNTkgMTIgNSAxNy41OSA2LjQxIDE5IDEyIDEzLjQxIDE3LjU5IDE5IDE5IDE3LjU5IDEzLjQxIDEyeiIvPgogIDwvZz4KCiAgPGcgY2xhc3M9ImpwLWljb24tbm9uZSBqcC1pY29uLWJ1c3kiIGZpbGw9Im5vbmUiPgogICAgPGNpcmNsZSBjeD0iMTIiIGN5PSIxMiIgcj0iNyIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-code: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjIiIGhlaWdodD0iMjIiIHZpZXdCb3g9IjAgMCAyOCAyOCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CgkJPHBhdGggZD0iTTExLjQgMTguNkw2LjggMTRMMTEuNCA5LjRMMTAgOEw0IDE0TDEwIDIwTDExLjQgMTguNlpNMTYuNiAxOC42TDIxLjIgMTRMMTYuNiA5LjRMMTggOEwyNCAxNEwxOCAyMEwxNi42IDE4LjZWMTguNloiLz4KCTwvZz4KPC9zdmc+Cg==);
  --jp-icon-console: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIwMCAyMDAiPgogIDxnIGNsYXNzPSJqcC1pY29uLWJyYW5kMSBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiMwMjg4RDEiPgogICAgPHBhdGggZD0iTTIwIDE5LjhoMTYwdjE1OS45SDIweiIvPgogIDwvZz4KICA8ZyBjbGFzcz0ianAtaWNvbi1zZWxlY3RhYmxlLWludmVyc2UiIGZpbGw9IiNmZmYiPgogICAgPHBhdGggZD0iTTEwNSAxMjcuM2g0MHYxMi44aC00MHpNNTEuMSA3N0w3NCA5OS45bC0yMy4zIDIzLjMgMTAuNSAxMC41IDIzLjMtMjMuM0w5NSA5OS45IDg0LjUgODkuNCA2MS42IDY2LjV6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-copy: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMTggMTgiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTExLjksMUgzLjJDMi40LDEsMS43LDEuNywxLjcsMi41djEwLjJoMS41VjIuNWg4LjdWMXogTTE0LjEsMy45aC04Yy0wLjgsMC0xLjUsMC43LTEuNSwxLjV2MTAuMmMwLDAuOCwwLjcsMS41LDEuNSwxLjVoOCBjMC44LDAsMS41LTAuNywxLjUtMS41VjUuNEMxNS41LDQuNiwxNC45LDMuOSwxNC4xLDMuOXogTTE0LjEsMTUuNWgtOFY1LjRoOFYxNS41eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-copyright: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIGVuYWJsZS1iYWNrZ3JvdW5kPSJuZXcgMCAwIDI0IDI0IiBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCI+CiAgPGcgY2xhc3M9ImpwLWljb24zIiBmaWxsPSIjNjE2MTYxIj4KICAgIDxwYXRoIGQ9Ik0xMS44OCw5LjE0YzEuMjgsMC4wNiwxLjYxLDEuMTUsMS42MywxLjY2aDEuNzljLTAuMDgtMS45OC0xLjQ5LTMuMTktMy40NS0zLjE5QzkuNjQsNy42MSw4LDksOCwxMi4xNCBjMCwxLjk0LDAuOTMsNC4yNCwzLjg0LDQuMjRjMi4yMiwwLDMuNDEtMS42NSwzLjQ0LTIuOTVoLTEuNzljLTAuMDMsMC41OS0wLjQ1LDEuMzgtMS42MywxLjQ0QzEwLjU1LDE0LjgzLDEwLDEzLjgxLDEwLDEyLjE0IEMxMCw5LjI1LDExLjI4LDkuMTYsMTEuODgsOS4xNHogTTEyLDJDNi40OCwyLDIsNi40OCwyLDEyczQuNDgsMTAsMTAsMTBzMTAtNC40OCwxMC0xMFMxNy41MiwyLDEyLDJ6IE0xMiwyMGMtNC40MSwwLTgtMy41OS04LTggczMuNTktOCw4LThzOCwzLjU5LDgsOFMxNi40MSwyMCwxMiwyMHoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-cut: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTkuNjQgNy42NGMuMjMtLjUuMzYtMS4wNS4zNi0xLjY0IDAtMi4yMS0xLjc5LTQtNC00UzIgMy43OSAyIDZzMS43OSA0IDQgNGMuNTkgMCAxLjE0LS4xMyAxLjY0LS4zNkwxMCAxMmwtMi4zNiAyLjM2QzcuMTQgMTQuMTMgNi41OSAxNCA2IDE0Yy0yLjIxIDAtNCAxLjc5LTQgNHMxLjc5IDQgNCA0IDQtMS43OSA0LTRjMC0uNTktLjEzLTEuMTQtLjM2LTEuNjRMMTIgMTRsNyA3aDN2LTFMOS42NCA3LjY0ek02IDhjLTEuMSAwLTItLjg5LTItMnMuOS0yIDItMiAyIC44OSAyIDItLjkgMi0yIDJ6bTAgMTJjLTEuMSAwLTItLjg5LTItMnMuOS0yIDItMiAyIC44OSAyIDItLjkgMi0yIDJ6bTYtNy41Yy0uMjggMC0uNS0uMjItLjUtLjVzLjIyLS41LjUtLjUuNS4yMi41LjUtLjIyLjUtLjUuNXpNMTkgM2wtNiA2IDIgMiA3LTdWM3oiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-download: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTE5IDloLTRWM0g5djZINWw3IDcgNy03ek01IDE4djJoMTR2LTJINXoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-edit: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTMgMTcuMjVWMjFoMy43NUwxNy44MSA5Ljk0bC0zLjc1LTMuNzVMMyAxNy4yNXpNMjAuNzEgNy4wNGMuMzktLjM5LjM5LTEuMDIgMC0xLjQxbC0yLjM0LTIuMzRjLS4zOS0uMzktMS4wMi0uMzktMS40MSAwbC0xLjgzIDEuODMgMy43NSAzLjc1IDEuODMtMS44M3oiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-ellipses: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPGNpcmNsZSBjeD0iNSIgY3k9IjEyIiByPSIyIi8+CiAgICA8Y2lyY2xlIGN4PSIxMiIgY3k9IjEyIiByPSIyIi8+CiAgICA8Y2lyY2xlIGN4PSIxOSIgY3k9IjEyIiByPSIyIi8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-extension: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTIwLjUgMTFIMTlWN2MwLTEuMS0uOS0yLTItMmgtNFYzLjVDMTMgMi4xMiAxMS44OCAxIDEwLjUgMVM4IDIuMTIgOCAzLjVWNUg0Yy0xLjEgMC0xLjk5LjktMS45OSAydjMuOEgzLjVjMS40OSAwIDIuNyAxLjIxIDIuNyAyLjdzLTEuMjEgMi43LTIuNyAyLjdIMlYyMGMwIDEuMS45IDIgMiAyaDMuOHYtMS41YzAtMS40OSAxLjIxLTIuNyAyLjctMi43IDEuNDkgMCAyLjcgMS4yMSAyLjcgMi43VjIySDE3YzEuMSAwIDItLjkgMi0ydi00aDEuNWMxLjM4IDAgMi41LTEuMTIgMi41LTIuNVMyMS44OCAxMSAyMC41IDExeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-fast-forward: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTQgMThsOC41LTZMNCA2djEyem05LTEydjEybDguNS02TDEzIDZ6Ii8+CiAgICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-file-upload: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTkgMTZoNnYtNmg0bC03LTctNyA3aDR6bS00IDJoMTR2Mkg1eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-file: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMTkuMyA4LjJsLTUuNS01LjVjLS4zLS4zLS43LS41LTEuMi0uNUgzLjljLS44LjEtMS42LjktMS42IDEuOHYxNC4xYzAgLjkuNyAxLjYgMS42IDEuNmgxNC4yYy45IDAgMS42LS43IDEuNi0xLjZWOS40Yy4xLS41LS4xLS45LS40LTEuMnptLTUuOC0zLjNsMy40IDMuNmgtMy40VjQuOXptMy45IDEyLjdINC43Yy0uMSAwLS4yIDAtLjItLjJWNC43YzAtLjIuMS0uMy4yLS4zaDcuMnY0LjRzMCAuOC4zIDEuMWMuMy4zIDEuMS4zIDEuMS4zaDQuM3Y3LjJzLS4xLjItLjIuMnoiLz4KPC9zdmc+Cg==);
  --jp-icon-filter-list: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTEwIDE4aDR2LTJoLTR2MnpNMyA2djJoMThWNkgzem0zIDdoMTJ2LTJINnYyeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-folder: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMTAgNEg0Yy0xLjEgMC0xLjk5LjktMS45OSAyTDIgMThjMCAxLjEuOSAyIDIgMmgxNmMxLjEgMCAyLS45IDItMlY4YzAtMS4xLS45LTItMi0yaC04bC0yLTJ6Ii8+Cjwvc3ZnPgo=);
  --jp-icon-html5: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDUxMiA1MTIiPgogIDxwYXRoIGNsYXNzPSJqcC1pY29uMCBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiMwMDAiIGQ9Ik0xMDguNCAwaDIzdjIyLjhoMjEuMlYwaDIzdjY5aC0yM1Y0NmgtMjF2MjNoLTIzLjJNMjA2IDIzaC0yMC4zVjBoNjMuN3YyM0gyMjl2NDZoLTIzbTUzLjUtNjloMjQuMWwxNC44IDI0LjNMMzEzLjIgMGgyNC4xdjY5aC0yM1YzNC44bC0xNi4xIDI0LjgtMTYuMS0yNC44VjY5aC0yMi42bTg5LjItNjloMjN2NDYuMmgzMi42VjY5aC01NS42Ii8+CiAgPHBhdGggY2xhc3M9ImpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iI2U0NGQyNiIgZD0iTTEwNy42IDQ3MWwtMzMtMzcwLjRoMzYyLjhsLTMzIDM3MC4yTDI1NS43IDUxMiIvPgogIDxwYXRoIGNsYXNzPSJqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiNmMTY1MjkiIGQ9Ik0yNTYgNDgwLjVWMTMxaDE0OC4zTDM3NiA0NDciLz4KICA8cGF0aCBjbGFzcz0ianAtaWNvbi1zZWxlY3RhYmxlLWludmVyc2UiIGZpbGw9IiNlYmViZWIiIGQ9Ik0xNDIgMTc2LjNoMTE0djQ1LjRoLTY0LjJsNC4yIDQ2LjVoNjB2NDUuM0gxNTQuNG0yIDIyLjhIMjAybDMuMiAzNi4zIDUwLjggMTMuNnY0Ny40bC05My4yLTI2Ii8+CiAgPHBhdGggY2xhc3M9ImpwLWljb24tc2VsZWN0YWJsZS1pbnZlcnNlIiBmaWxsPSIjZmZmIiBkPSJNMzY5LjYgMTc2LjNIMjU1Ljh2NDUuNGgxMDkuNm0tNC4xIDQ2LjVIMjU1Ljh2NDUuNGg1NmwtNS4zIDU5LTUwLjcgMTMuNnY0Ny4ybDkzLTI1LjgiLz4KPC9zdmc+Cg==);
  --jp-icon-image: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8cGF0aCBjbGFzcz0ianAtaWNvbi1icmFuZDQganAtaWNvbi1zZWxlY3RhYmxlLWludmVyc2UiIGZpbGw9IiNGRkYiIGQ9Ik0yLjIgMi4yaDE3LjV2MTcuNUgyLjJ6Ii8+CiAgPHBhdGggY2xhc3M9ImpwLWljb24tYnJhbmQwIGpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iIzNGNTFCNSIgZD0iTTIuMiAyLjJ2MTcuNWgxNy41bC4xLTE3LjVIMi4yem0xMi4xIDIuMmMxLjIgMCAyLjIgMSAyLjIgMi4ycy0xIDIuMi0yLjIgMi4yLTIuMi0xLTIuMi0yLjIgMS0yLjIgMi4yLTIuMnpNNC40IDE3LjZsMy4zLTguOCAzLjMgNi42IDIuMi0zLjIgNC40IDUuNEg0LjR6Ii8+Cjwvc3ZnPgo=);
  --jp-icon-inspector: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMjAgNEg0Yy0xLjEgMC0xLjk5LjktMS45OSAyTDIgMThjMCAxLjEuOSAyIDIgMmgxNmMxLjEgMCAyLS45IDItMlY2YzAtMS4xLS45LTItMi0yem0tNSAxNEg0di00aDExdjR6bTAtNUg0VjloMTF2NHptNSA1aC00VjloNHY5eiIvPgo8L3N2Zz4K);
  --jp-icon-json: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8ZyBjbGFzcz0ianAtaWNvbi13YXJuMSBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiNGOUE4MjUiPgogICAgPHBhdGggZD0iTTIwLjIgMTEuOGMtMS42IDAtMS43LjUtMS43IDEgMCAuNC4xLjkuMSAxLjMuMS41LjEuOS4xIDEuMyAwIDEuNy0xLjQgMi4zLTMuNSAyLjNoLS45di0xLjloLjVjMS4xIDAgMS40IDAgMS40LS44IDAtLjMgMC0uNi0uMS0xIDAtLjQtLjEtLjgtLjEtMS4yIDAtMS4zIDAtMS44IDEuMy0yLTEuMy0uMi0xLjMtLjctMS4zLTIgMC0uNC4xLS44LjEtMS4yLjEtLjQuMS0uNy4xLTEgMC0uOC0uNC0uNy0xLjQtLjhoLS41VjQuMWguOWMyLjIgMCAzLjUuNyAzLjUgMi4zIDAgLjQtLjEuOS0uMSAxLjMtLjEuNS0uMS45LS4xIDEuMyAwIC41LjIgMSAxLjcgMXYxLjh6TTEuOCAxMC4xYzEuNiAwIDEuNy0uNSAxLjctMSAwLS40LS4xLS45LS4xLTEuMy0uMS0uNS0uMS0uOS0uMS0xLjMgMC0xLjYgMS40LTIuMyAzLjUtMi4zaC45djEuOWgtLjVjLTEgMC0xLjQgMC0xLjQuOCAwIC4zIDAgLjYuMSAxIDAgLjIuMS42LjEgMSAwIDEuMyAwIDEuOC0xLjMgMkM2IDExLjIgNiAxMS43IDYgMTNjMCAuNC0uMS44LS4xIDEuMi0uMS4zLS4xLjctLjEgMSAwIC44LjMuOCAxLjQuOGguNXYxLjloLS45Yy0yLjEgMC0zLjUtLjYtMy41LTIuMyAwLS40LjEtLjkuMS0xLjMuMS0uNS4xLS45LjEtMS4zIDAtLjUtLjItMS0xLjctMXYtMS45eiIvPgogICAgPGNpcmNsZSBjeD0iMTEiIGN5PSIxMy44IiByPSIyLjEiLz4KICAgIDxjaXJjbGUgY3g9IjExIiBjeT0iOC4yIiByPSIyLjEiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-julia: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDMyNSAzMDAiPgogIDxnIGNsYXNzPSJqcC1icmFuZDAganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjY2IzYzMzIj4KICAgIDxwYXRoIGQ9Ik0gMTUwLjg5ODQzOCAyMjUgQyAxNTAuODk4NDM4IDI2Ni40MjE4NzUgMTE3LjMyMDMxMiAzMDAgNzUuODk4NDM4IDMwMCBDIDM0LjQ3NjU2MiAzMDAgMC44OTg0MzggMjY2LjQyMTg3NSAwLjg5ODQzOCAyMjUgQyAwLjg5ODQzOCAxODMuNTc4MTI1IDM0LjQ3NjU2MiAxNTAgNzUuODk4NDM4IDE1MCBDIDExNy4zMjAzMTIgMTUwIDE1MC44OTg0MzggMTgzLjU3ODEyNSAxNTAuODk4NDM4IDIyNSIvPgogIDwvZz4KICA8ZyBjbGFzcz0ianAtYnJhbmQwIGpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iIzM4OTgyNiI+CiAgICA8cGF0aCBkPSJNIDIzNy41IDc1IEMgMjM3LjUgMTE2LjQyMTg3NSAyMDMuOTIxODc1IDE1MCAxNjIuNSAxNTAgQyAxMjEuMDc4MTI1IDE1MCA4Ny41IDExNi40MjE4NzUgODcuNSA3NSBDIDg3LjUgMzMuNTc4MTI1IDEyMS4wNzgxMjUgMCAxNjIuNSAwIEMgMjAzLjkyMTg3NSAwIDIzNy41IDMzLjU3ODEyNSAyMzcuNSA3NSIvPgogIDwvZz4KICA8ZyBjbGFzcz0ianAtYnJhbmQwIGpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iIzk1NThiMiI+CiAgICA8cGF0aCBkPSJNIDMyNC4xMDE1NjIgMjI1IEMgMzI0LjEwMTU2MiAyNjYuNDIxODc1IDI5MC41MjM0MzggMzAwIDI0OS4xMDE1NjIgMzAwIEMgMjA3LjY3OTY4OCAzMDAgMTc0LjEwMTU2MiAyNjYuNDIxODc1IDE3NC4xMDE1NjIgMjI1IEMgMTc0LjEwMTU2MiAxODMuNTc4MTI1IDIwNy42Nzk2ODggMTUwIDI0OS4xMDE1NjIgMTUwIEMgMjkwLjUyMzQzOCAxNTAgMzI0LjEwMTU2MiAxODMuNTc4MTI1IDMyNC4xMDE1NjIgMjI1Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-jupyter-favicon: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTUyIiBoZWlnaHQ9IjE2NSIgdmlld0JveD0iMCAwIDE1MiAxNjUiIHZlcnNpb249IjEuMSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbi13YXJuMCIgZmlsbD0iI0YzNzcyNiI+CiAgICA8cGF0aCB0cmFuc2Zvcm09InRyYW5zbGF0ZSgwLjA3ODk0NywgMTEwLjU4MjkyNykiIGQ9Ik03NS45NDIyODQyLDI5LjU4MDQ1NjEgQzQzLjMwMjM5NDcsMjkuNTgwNDU2MSAxNC43OTY3ODMyLDE3LjY1MzQ2MzQgMCwwIEM1LjUxMDgzMjExLDE1Ljg0MDY4MjkgMTUuNzgxNTM4OSwyOS41NjY3NzMyIDI5LjM5MDQ5NDcsMzkuMjc4NDE3MSBDNDIuOTk5Nyw0OC45ODk4NTM3IDU5LjI3MzcsNTQuMjA2NzgwNSA3NS45NjA1Nzg5LDU0LjIwNjc4MDUgQzkyLjY0NzQ1NzksNTQuMjA2NzgwNSAxMDguOTIxNDU4LDQ4Ljk4OTg1MzcgMTIyLjUzMDY2MywzOS4yNzg0MTcxIEMxMzYuMTM5NDUzLDI5LjU2Njc3MzIgMTQ2LjQxMDI4NCwxNS44NDA2ODI5IDE1MS45MjExNTgsMCBDMTM3LjA4Nzg2OCwxNy42NTM0NjM0IDEwOC41ODI1ODksMjkuNTgwNDU2MSA3NS45NDIyODQyLDI5LjU4MDQ1NjEgTDc1Ljk0MjI4NDIsMjkuNTgwNDU2MSBaIiAvPgogICAgPHBhdGggdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMC4wMzczNjgsIDAuNzA0ODc4KSIgZD0iTTc1Ljk3ODQ1NzksMjQuNjI2NDA3MyBDMTA4LjYxODc2MywyNC42MjY0MDczIDEzNy4xMjQ0NTgsMzYuNTUzNDQxNSAxNTEuOTIxMTU4LDU0LjIwNjc4MDUgQzE0Ni40MTAyODQsMzguMzY2MjIyIDEzNi4xMzk0NTMsMjQuNjQwMTMxNyAxMjIuNTMwNjYzLDE0LjkyODQ4NzggQzEwOC45MjE0NTgsNS4yMTY4NDM5IDkyLjY0NzQ1NzksMCA3NS45NjA1Nzg5LDAgQzU5LjI3MzcsMCA0Mi45OTk3LDUuMjE2ODQzOSAyOS4zOTA0OTQ3LDE0LjkyODQ4NzggQzE1Ljc4MTUzODksMjQuNjQwMTMxNyA1LjUxMDgzMjExLDM4LjM2NjIyMiAwLDU0LjIwNjc4MDUgQzE0LjgzMzA4MTYsMzYuNTg5OTI5MyA0My4zMzg1Njg0LDI0LjYyNjQwNzMgNzUuOTc4NDU3OSwyNC42MjY0MDczIEw3NS45Nzg0NTc5LDI0LjYyNjQwNzMgWiIgLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-jupyter: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMzkiIGhlaWdodD0iNTEiIHZpZXdCb3g9IjAgMCAzOSA1MSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSgtMTYzOCAtMjI4MSkiPgogICAgPGcgY2xhc3M9ImpwLWljb24td2FybjAiIGZpbGw9IiNGMzc3MjYiPgogICAgICA8cGF0aCB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxNjM5Ljc0IDIzMTEuOTgpIiBkPSJNIDE4LjI2NDYgNy4xMzQxMUMgMTAuNDE0NSA3LjEzNDExIDMuNTU4NzIgNC4yNTc2IDAgMEMgMS4zMjUzOSAzLjgyMDQgMy43OTU1NiA3LjEzMDgxIDcuMDY4NiA5LjQ3MzAzQyAxMC4zNDE3IDExLjgxNTIgMTQuMjU1NyAxMy4wNzM0IDE4LjI2OSAxMy4wNzM0QyAyMi4yODIzIDEzLjA3MzQgMjYuMTk2MyAxMS44MTUyIDI5LjQ2OTQgOS40NzMwM0MgMzIuNzQyNCA3LjEzMDgxIDM1LjIxMjYgMy44MjA0IDM2LjUzOCAwQyAzMi45NzA1IDQuMjU3NiAyNi4xMTQ4IDcuMTM0MTEgMTguMjY0NiA3LjEzNDExWiIvPgogICAgICA8cGF0aCB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxNjM5LjczIDIyODUuNDgpIiBkPSJNIDE4LjI3MzMgNS45MzkzMUMgMjYuMTIzNSA1LjkzOTMxIDMyLjk3OTMgOC44MTU4MyAzNi41MzggMTMuMDczNEMgMzUuMjEyNiA5LjI1MzAzIDMyLjc0MjQgNS45NDI2MiAyOS40Njk0IDMuNjAwNEMgMjYuMTk2MyAxLjI1ODE4IDIyLjI4MjMgMCAxOC4yNjkgMEMgMTQuMjU1NyAwIDEwLjM0MTcgMS4yNTgxOCA3LjA2ODYgMy42MDA0QyAzLjc5NTU2IDUuOTQyNjIgMS4zMjUzOSA5LjI1MzAzIDAgMTMuMDczNEMgMy41Njc0NSA4LjgyNDYzIDEwLjQyMzIgNS45MzkzMSAxOC4yNzMzIDUuOTM5MzFaIi8+CiAgICA8L2c+CiAgICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgICA8cGF0aCB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxNjY5LjMgMjI4MS4zMSkiIGQ9Ik0gNS44OTM1MyAyLjg0NEMgNS45MTg4OSAzLjQzMTY1IDUuNzcwODUgNC4wMTM2NyA1LjQ2ODE1IDQuNTE2NDVDIDUuMTY1NDUgNS4wMTkyMiA0LjcyMTY4IDUuNDIwMTUgNC4xOTI5OSA1LjY2ODUxQyAzLjY2NDMgNS45MTY4OCAzLjA3NDQ0IDYuMDAxNTEgMi40OTgwNSA1LjkxMTcxQyAxLjkyMTY2IDUuODIxOSAxLjM4NDYzIDUuNTYxNyAwLjk1NDg5OCA1LjE2NDAxQyAwLjUyNTE3IDQuNzY2MzMgMC4yMjIwNTYgNC4yNDkwMyAwLjA4MzkwMzcgMy42Nzc1N0MgLTAuMDU0MjQ4MyAzLjEwNjExIC0wLjAyMTIzIDIuNTA2MTcgMC4xNzg3ODEgMS45NTM2NEMgMC4zNzg3OTMgMS40MDExIDAuNzM2ODA5IDAuOTIwODE3IDEuMjA3NTQgMC41NzM1MzhDIDEuNjc4MjYgMC4yMjYyNTkgMi4yNDA1NSAwLjAyNzU5MTkgMi44MjMyNiAwLjAwMjY3MjI5QyAzLjYwMzg5IC0wLjAzMDcxMTUgNC4zNjU3MyAwLjI0OTc4OSA0Ljk0MTQyIDAuNzgyNTUxQyA1LjUxNzExIDEuMzE1MzEgNS44NTk1NiAyLjA1Njc2IDUuODkzNTMgMi44NDRaIi8+CiAgICAgIDxwYXRoIHRyYW5zZm9ybT0idHJhbnNsYXRlKDE2MzkuOCAyMzIzLjgxKSIgZD0iTSA3LjQyNzg5IDMuNTgzMzhDIDcuNDYwMDggNC4zMjQzIDcuMjczNTUgNS4wNTgxOSA2Ljg5MTkzIDUuNjkyMTNDIDYuNTEwMzEgNi4zMjYwNyA1Ljk1MDc1IDYuODMxNTYgNS4yODQxMSA3LjE0NDZDIDQuNjE3NDcgNy40NTc2MyAzLjg3MzcxIDcuNTY0MTQgMy4xNDcwMiA3LjQ1MDYzQyAyLjQyMDMyIDcuMzM3MTIgMS43NDMzNiA3LjAwODcgMS4yMDE4NCA2LjUwNjk1QyAwLjY2MDMyOCA2LjAwNTIgMC4yNzg2MSA1LjM1MjY4IDAuMTA1MDE3IDQuNjMyMDJDIC0wLjA2ODU3NTcgMy45MTEzNSAtMC4wMjYyMzYxIDMuMTU0OTQgMC4yMjY2NzUgMi40NTg1NkMgMC40Nzk1ODcgMS43NjIxNyAwLjkzMTY5NyAxLjE1NzEzIDEuNTI1NzYgMC43MjAwMzNDIDIuMTE5ODMgMC4yODI5MzUgMi44MjkxNCAwLjAzMzQzOTUgMy41NjM4OSAwLjAwMzEzMzQ0QyA0LjU0NjY3IC0wLjAzNzQwMzMgNS41MDUyOSAwLjMxNjcwNiA2LjIyOTYxIDAuOTg3ODM1QyA2Ljk1MzkzIDEuNjU4OTYgNy4zODQ4NCAyLjU5MjM1IDcuNDI3ODkgMy41ODMzOEwgNy40Mjc4OSAzLjU4MzM4WiIvPgogICAgICA8cGF0aCB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxNjM4LjM2IDIyODYuMDYpIiBkPSJNIDIuMjc0NzEgNC4zOTYyOUMgMS44NDM2MyA0LjQxNTA4IDEuNDE2NzEgNC4zMDQ0NSAxLjA0Nzk5IDQuMDc4NDNDIDAuNjc5MjY4IDMuODUyNCAwLjM4NTMyOCAzLjUyMTE0IDAuMjAzMzcxIDMuMTI2NTZDIDAuMDIxNDEzNiAyLjczMTk4IC0wLjA0MDM3OTggMi4yOTE4MyAwLjAyNTgxMTYgMS44NjE4MUMgMC4wOTIwMDMxIDEuNDMxOCAwLjI4MzIwNCAxLjAzMTI2IDAuNTc1MjEzIDAuNzEwODgzQyAwLjg2NzIyMiAwLjM5MDUxIDEuMjQ2OTEgMC4xNjQ3MDggMS42NjYyMiAwLjA2MjA1OTJDIDIuMDg1NTMgLTAuMDQwNTg5NyAyLjUyNTYxIC0wLjAxNTQ3MTQgMi45MzA3NiAwLjEzNDIzNUMgMy4zMzU5MSAwLjI4Mzk0MSAzLjY4NzkyIDAuNTUxNTA1IDMuOTQyMjIgMC45MDMwNkMgNC4xOTY1MiAxLjI1NDYyIDQuMzQxNjkgMS42NzQzNiA0LjM1OTM1IDIuMTA5MTZDIDQuMzgyOTkgMi42OTEwNyA0LjE3Njc4IDMuMjU4NjkgMy43ODU5NyAzLjY4NzQ2QyAzLjM5NTE2IDQuMTE2MjQgMi44NTE2NiA0LjM3MTE2IDIuMjc0NzEgNC4zOTYyOUwgMi4yNzQ3MSA0LjM5NjI5WiIvPgogICAgPC9nPgogIDwvZz4+Cjwvc3ZnPgo=);
  --jp-icon-jupyterlab-wordmark: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyMDAiIHZpZXdCb3g9IjAgMCAxODYwLjggNDc1Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjIiIGZpbGw9IiM0RTRFNEUiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDQ4MC4xMzY0MDEsIDY0LjI3MTQ5MykiPgogICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMC4wMDAwMDAsIDU4Ljg3NTU2NikiPgogICAgICA8ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSgwLjA4NzYwMywgMC4xNDAyOTQpIj4KICAgICAgICA8cGF0aCBkPSJNLTQyNi45LDE2OS44YzAsNDguNy0zLjcsNjQuNy0xMy42LDc2LjRjLTEwLjgsMTAtMjUsMTUuNS0zOS43LDE1LjVsMy43LDI5IGMyMi44LDAuMyw0NC44LTcuOSw2MS45LTIzLjFjMTcuOC0xOC41LDI0LTQ0LjEsMjQtODMuM1YwSC00Mjd2MTcwLjFMLTQyNi45LDE2OS44TC00MjYuOSwxNjkuOHoiLz4KICAgICAgPC9nPgogICAgPC9nPgogICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMTU1LjA0NTI5NiwgNTYuODM3MTA0KSI+CiAgICAgIDxnIHRyYW5zZm9ybT0idHJhbnNsYXRlKDEuNTYyNDUzLCAxLjc5OTg0MikiPgogICAgICAgIDxwYXRoIGQ9Ik0tMzEyLDE0OGMwLDIxLDAsMzkuNSwxLjcsNTUuNGgtMzEuOGwtMi4xLTMzLjNoLTAuOGMtNi43LDExLjYtMTYuNCwyMS4zLTI4LDI3LjkgYy0xMS42LDYuNi0yNC44LDEwLTM4LjIsOS44Yy0zMS40LDAtNjktMTcuNy02OS04OVYwaDM2LjR2MTEyLjdjMCwzOC43LDExLjYsNjQuNyw0NC42LDY0LjdjMTAuMy0wLjIsMjAuNC0zLjUsMjguOS05LjQgYzguNS01LjksMTUuMS0xNC4zLDE4LjktMjMuOWMyLjItNi4xLDMuMy0xMi41LDMuMy0xOC45VjAuMmgzNi40VjE0OEgtMzEyTC0zMTIsMTQ4eiIvPgogICAgICA8L2c+CiAgICA8L2c+CiAgICA8ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSgzOTAuMDEzMzIyLCA1My40Nzk2MzgpIj4KICAgICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMS43MDY0NTgsIDAuMjMxNDI1KSI+CiAgICAgICAgPHBhdGggZD0iTS00NzguNiw3MS40YzAtMjYtMC44LTQ3LTEuNy02Ni43aDMyLjdsMS43LDM0LjhoMC44YzcuMS0xMi41LDE3LjUtMjIuOCwzMC4xLTI5LjcgYzEyLjUtNywyNi43LTEwLjMsNDEtOS44YzQ4LjMsMCw4NC43LDQxLjcsODQuNywxMDMuM2MwLDczLjEtNDMuNywxMDkuMi05MSwxMDkuMmMtMTIuMSwwLjUtMjQuMi0yLjItMzUtNy44IGMtMTAuOC01LjYtMTkuOS0xMy45LTI2LjYtMjQuMmgtMC44VjI5MWgtMzZ2LTIyMEwtNDc4LjYsNzEuNEwtNDc4LjYsNzEuNHogTS00NDIuNiwxMjUuNmMwLjEsNS4xLDAuNiwxMC4xLDEuNywxNS4xIGMzLDEyLjMsOS45LDIzLjMsMTkuOCwzMS4xYzkuOSw3LjgsMjIuMSwxMi4xLDM0LjcsMTIuMWMzOC41LDAsNjAuNy0zMS45LDYwLjctNzguNWMwLTQwLjctMjEuMS03NS42LTU5LjUtNzUuNiBjLTEyLjksMC40LTI1LjMsNS4xLTM1LjMsMTMuNGMtOS45LDguMy0xNi45LDE5LjctMTkuNiwzMi40Yy0xLjUsNC45LTIuMywxMC0yLjUsMTUuMVYxMjUuNkwtNDQyLjYsMTI1LjZMLTQ0Mi42LDEyNS42eiIvPgogICAgICA8L2c+CiAgICA8L2c+CiAgICA8ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSg2MDYuNzQwNzI2LCA1Ni44MzcxMDQpIj4KICAgICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMC43NTEyMjYsIDEuOTg5Mjk5KSI+CiAgICAgICAgPHBhdGggZD0iTS00NDAuOCwwbDQzLjcsMTIwLjFjNC41LDEzLjQsOS41LDI5LjQsMTIuOCw0MS43aDAuOGMzLjctMTIuMiw3LjktMjcuNywxMi44LTQyLjQgbDM5LjctMTE5LjJoMzguNUwtMzQ2LjksMTQ1Yy0yNiw2OS43LTQzLjcsMTA1LjQtNjguNiwxMjcuMmMtMTIuNSwxMS43LTI3LjksMjAtNDQuNiwyMy45bC05LjEtMzEuMSBjMTEuNy0zLjksMjIuNS0xMC4xLDMxLjgtMTguMWMxMy4yLTExLjEsMjMuNy0yNS4yLDMwLjYtNDEuMmMxLjUtMi44LDIuNS01LjcsMi45LTguOGMtMC4zLTMuMy0xLjItNi42LTIuNS05LjdMLTQ4MC4yLDAuMSBoMzkuN0wtNDQwLjgsMEwtNDQwLjgsMHoiLz4KICAgICAgPC9nPgogICAgPC9nPgogICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoODIyLjc0ODEwNCwgMC4wMDAwMDApIj4KICAgICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMS40NjQwNTAsIDAuMzc4OTE0KSI+CiAgICAgICAgPHBhdGggZD0iTS00MTMuNywwdjU4LjNoNTJ2MjguMmgtNTJWMTk2YzAsMjUsNywzOS41LDI3LjMsMzkuNWM3LjEsMC4xLDE0LjItMC43LDIxLjEtMi41IGwxLjcsMjcuN2MtMTAuMywzLjctMjEuMyw1LjQtMzIuMiw1Yy03LjMsMC40LTE0LjYtMC43LTIxLjMtMy40Yy02LjgtMi43LTEyLjktNi44LTE3LjktMTIuMWMtMTAuMy0xMC45LTE0LjEtMjktMTQuMS01Mi45IFY4Ni41aC0zMVY1OC4zaDMxVjkuNkwtNDEzLjcsMEwtNDEzLjcsMHoiLz4KICAgICAgPC9nPgogICAgPC9nPgogICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoOTc0LjQzMzI4NiwgNTMuNDc5NjM4KSI+CiAgICAgIDxnIHRyYW5zZm9ybT0idHJhbnNsYXRlKDAuOTkwMDM0LCAwLjYxMDMzOSkiPgogICAgICAgIDxwYXRoIGQ9Ik0tNDQ1LjgsMTEzYzAuOCw1MCwzMi4yLDcwLjYsNjguNiw3MC42YzE5LDAuNiwzNy45LTMsNTUuMy0xMC41bDYuMiwyNi40IGMtMjAuOSw4LjktNDMuNSwxMy4xLTY2LjIsMTIuNmMtNjEuNSwwLTk4LjMtNDEuMi05OC4zLTEwMi41Qy00ODAuMiw0OC4yLTQ0NC43LDAtMzg2LjUsMGM2NS4yLDAsODIuNyw1OC4zLDgyLjcsOTUuNyBjLTAuMSw1LjgtMC41LDExLjUtMS4yLDE3LjJoLTE0MC42SC00NDUuOEwtNDQ1LjgsMTEzeiBNLTMzOS4yLDg2LjZjMC40LTIzLjUtOS41LTYwLjEtNTAuNC02MC4xIGMtMzYuOCwwLTUyLjgsMzQuNC01NS43LDYwLjFILTMzOS4yTC0zMzkuMiw4Ni42TC0zMzkuMiw4Ni42eiIvPgogICAgICA8L2c+CiAgICA8L2c+CiAgICA8ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxMjAxLjk2MTA1OCwgNTMuNDc5NjM4KSI+CiAgICAgIDxnIHRyYW5zZm9ybT0idHJhbnNsYXRlKDEuMTc5NjQwLCAwLjcwNTA2OCkiPgogICAgICAgIDxwYXRoIGQ9Ik0tNDc4LjYsNjhjMC0yMy45LTAuNC00NC41LTEuNy02My40aDMxLjhsMS4yLDM5LjloMS43YzkuMS0yNy4zLDMxLTQ0LjUsNTUuMy00NC41IGMzLjUtMC4xLDcsMC40LDEwLjMsMS4ydjM0LjhjLTQuMS0wLjktOC4yLTEuMy0xMi40LTEuMmMtMjUuNiwwLTQzLjcsMTkuNy00OC43LDQ3LjRjLTEsNS43LTEuNiwxMS41LTEuNywxNy4ydjEwOC4zaC0zNlY2OCBMLTQ3OC42LDY4eiIvPgogICAgICA8L2c+CiAgICA8L2c+CiAgPC9nPgoKICA8ZyBjbGFzcz0ianAtaWNvbi13YXJuMCIgZmlsbD0iI0YzNzcyNiI+CiAgICA8cGF0aCBkPSJNMTM1Mi4zLDMyNi4yaDM3VjI4aC0zN1YzMjYuMnogTTE2MDQuOCwzMjYuMmMtMi41LTEzLjktMy40LTMxLjEtMy40LTQ4Ljd2LTc2IGMwLTQwLjctMTUuMS04My4xLTc3LjMtODMuMWMtMjUuNiwwLTUwLDcuMS02Ni44LDE4LjFsOC40LDI0LjRjMTQuMy05LjIsMzQtMTUuMSw1My0xNS4xYzQxLjYsMCw0Ni4yLDMwLjIsNDYuMiw0N3Y0LjIgYy03OC42LTAuNC0xMjIuMywyNi41LTEyMi4zLDc1LjZjMCwyOS40LDIxLDU4LjQsNjIuMiw1OC40YzI5LDAsNTAuOS0xNC4zLDYyLjItMzAuMmgxLjNsMi45LDI1LjZIMTYwNC44eiBNMTU2NS43LDI1Ny43IGMwLDMuOC0wLjgsOC0yLjEsMTEuOGMtNS45LDE3LjItMjIuNywzNC00OS4yLDM0Yy0xOC45LDAtMzQuOS0xMS4zLTM0LjktMzUuM2MwLTM5LjUsNDUuOC00Ni42LDg2LjItNDUuOFYyNTcuN3ogTTE2OTguNSwzMjYuMiBsMS43LTMzLjZoMS4zYzE1LjEsMjYuOSwzOC43LDM4LjIsNjguMSwzOC4yYzQ1LjQsMCw5MS4yLTM2LjEsOTEuMi0xMDguOGMwLjQtNjEuNy0zNS4zLTEwMy43LTg1LjctMTAzLjcgYy0zMi44LDAtNTYuMywxNC43LTY5LjMsMzcuNGgtMC44VjI4aC0zNi42djI0NS43YzAsMTguMS0wLjgsMzguNi0xLjcsNTIuNUgxNjk4LjV6IE0xNzA0LjgsMjA4LjJjMC01LjksMS4zLTEwLjksMi4xLTE1LjEgYzcuNi0yOC4xLDMxLjEtNDUuNCw1Ni4zLTQ1LjRjMzkuNSwwLDYwLjUsMzQuOSw2MC41LDc1LjZjMCw0Ni42LTIzLjEsNzguMS02MS44LDc4LjFjLTI2LjksMC00OC4zLTE3LjYtNTUuNS00My4zIGMtMC44LTQuMi0xLjctOC44LTEuNy0xMy40VjIwOC4yeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-kernel: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uMiIgZmlsbD0iIzYxNjE2MSIgZD0iTTE1IDlIOXY2aDZWOXptLTIgNGgtMnYtMmgydjJ6bTgtMlY5aC0yVjdjMC0xLjEtLjktMi0yLTJoLTJWM2gtMnYyaC0yVjNIOXYySDdjLTEuMSAwLTIgLjktMiAydjJIM3YyaDJ2MkgzdjJoMnYyYzAgMS4xLjkgMiAyIDJoMnYyaDJ2LTJoMnYyaDJ2LTJoMmMxLjEgMCAyLS45IDItMnYtMmgydi0yaC0ydi0yaDJ6bS00IDZIN1Y3aDEwdjEweiIvPgo8L3N2Zz4K);
  --jp-icon-keyboard: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMjAgNUg0Yy0xLjEgMC0xLjk5LjktMS45OSAyTDIgMTdjMCAxLjEuOSAyIDIgMmgxNmMxLjEgMCAyLS45IDItMlY3YzAtMS4xLS45LTItMi0yem0tOSAzaDJ2MmgtMlY4em0wIDNoMnYyaC0ydi0yek04IDhoMnYySDhWOHptMCAzaDJ2Mkg4di0yem0tMSAySDV2LTJoMnYyem0wLTNINVY4aDJ2MnptOSA3SDh2LTJoOHYyem0wLTRoLTJ2LTJoMnYyem0wLTNoLTJWOGgydjJ6bTMgM2gtMnYtMmgydjJ6bTAtM2gtMlY4aDJ2MnoiLz4KPC9zdmc+Cg==);
  --jp-icon-launcher: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMTkgMTlINVY1aDdWM0g1YTIgMiAwIDAwLTIgMnYxNGEyIDIgMCAwMDIgMmgxNGMxLjEgMCAyLS45IDItMnYtN2gtMnY3ek0xNCAzdjJoMy41OWwtOS44MyA5LjgzIDEuNDEgMS40MUwxOSA2LjQxVjEwaDJWM2gtN3oiLz4KPC9zdmc+Cg==);
  --jp-icon-line-form: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICAgIDxwYXRoIGZpbGw9IndoaXRlIiBkPSJNNS44OCA0LjEyTDEzLjc2IDEybC03Ljg4IDcuODhMOCAyMmwxMC0xMEw4IDJ6Ii8+Cjwvc3ZnPgo=);
  --jp-icon-link: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTMuOSAxMmMwLTEuNzEgMS4zOS0zLjEgMy4xLTMuMWg0VjdIN2MtMi43NiAwLTUgMi4yNC01IDVzMi4yNCA1IDUgNWg0di0xLjlIN2MtMS43MSAwLTMuMS0xLjM5LTMuMS0zLjF6TTggMTNoOHYtMkg4djJ6bTktNmgtNHYxLjloNGMxLjcxIDAgMy4xIDEuMzkgMy4xIDMuMXMtMS4zOSAzLjEtMy4xIDMuMWgtNFYxN2g0YzIuNzYgMCA1LTIuMjQgNS01cy0yLjI0LTUtNS01eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-list: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uMiBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiM2MTYxNjEiIGQ9Ik0xOSA1djE0SDVWNWgxNG0xLjEtMkgzLjljLS41IDAtLjkuNC0uOS45djE2LjJjMCAuNC40LjkuOS45aDE2LjJjLjQgMCAuOS0uNS45LS45VjMuOWMwLS41LS41LS45LS45LS45ek0xMSA3aDZ2MmgtNlY3em0wIDRoNnYyaC02di0yem0wIDRoNnYyaC02ek03IDdoMnYySDd6bTAgNGgydjJIN3ptMCA0aDJ2Mkg3eiIvPgo8L3N2Zz4=);
  --jp-icon-listings-info: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCA1MC45NzggNTAuOTc4IiBzdHlsZT0iZW5hYmxlLWJhY2tncm91bmQ6bmV3IDAgMCA1MC45NzggNTAuOTc4OyIgeG1sOnNwYWNlPSJwcmVzZXJ2ZSI+Cgk8Zz4KCQk8cGF0aCBzdHlsZT0iZmlsbDojMDEwMDAyOyIgZD0iTTQzLjUyLDcuNDU4QzM4LjcxMSwyLjY0OCwzMi4zMDcsMCwyNS40ODksMEMxOC42NywwLDEyLjI2NiwyLjY0OCw3LjQ1OCw3LjQ1OAoJCQljLTkuOTQzLDkuOTQxLTkuOTQzLDI2LjExOSwwLDM2LjA2MmM0LjgwOSw0LjgwOSwxMS4yMTIsNy40NTYsMTguMDMxLDcuNDU4YzAsMCwwLjAwMSwwLDAuMDAyLDAKCQkJYzYuODE2LDAsMTMuMjIxLTIuNjQ4LDE4LjAyOS03LjQ1OGM0LjgwOS00LjgwOSw3LjQ1Ny0xMS4yMTIsNy40NTctMTguMDNDNTAuOTc3LDE4LjY3LDQ4LjMyOCwxMi4yNjYsNDMuNTIsNy40NTh6CgkJCSBNNDIuMTA2LDQyLjEwNWMtNC40MzIsNC40MzEtMTAuMzMyLDYuODcyLTE2LjYxNSw2Ljg3MmgtMC4wMDJjLTYuMjg1LTAuMDAxLTEyLjE4Ny0yLjQ0MS0xNi42MTctNi44NzIKCQkJYy05LjE2Mi05LjE2My05LjE2Mi0yNC4wNzEsMC0zMy4yMzNDMTMuMzAzLDQuNDQsMTkuMjA0LDIsMjUuNDg5LDJjNi4yODQsMCwxMi4xODYsMi40NCwxNi42MTcsNi44NzIKCQkJYzQuNDMxLDQuNDMxLDYuODcxLDEwLjMzMiw2Ljg3MSwxNi42MTdDNDguOTc3LDMxLjc3Miw0Ni41MzYsMzcuNjc1LDQyLjEwNiw0Mi4xMDV6Ii8+CgkJPHBhdGggc3R5bGU9ImZpbGw6IzAxMDAwMjsiIGQ9Ik0yMy41NzgsMzIuMjE4Yy0wLjAyMy0xLjczNCwwLjE0My0zLjA1OSwwLjQ5Ni0zLjk3MmMwLjM1My0wLjkxMywxLjExLTEuOTk3LDIuMjcyLTMuMjUzCgkJCWMwLjQ2OC0wLjUzNiwwLjkyMy0xLjA2MiwxLjM2Ny0xLjU3NWMwLjYyNi0wLjc1MywxLjEwNC0xLjQ3OCwxLjQzNi0yLjE3NWMwLjMzMS0wLjcwNywwLjQ5NS0xLjU0MSwwLjQ5NS0yLjUKCQkJYzAtMS4wOTYtMC4yNi0yLjA4OC0wLjc3OS0yLjk3OWMtMC41NjUtMC44NzktMS41MDEtMS4zMzYtMi44MDYtMS4zNjljLTEuODAyLDAuMDU3LTIuOTg1LDAuNjY3LTMuNTUsMS44MzIKCQkJYy0wLjMwMSwwLjUzNS0wLjUwMywxLjE0MS0wLjYwNywxLjgxNGMtMC4xMzksMC43MDctMC4yMDcsMS40MzItMC4yMDcsMi4xNzRoLTIuOTM3Yy0wLjA5MS0yLjIwOCwwLjQwNy00LjExNCwxLjQ5My01LjcxOQoJCQljMS4wNjItMS42NCwyLjg1NS0yLjQ4MSw1LjM3OC0yLjUyN2MyLjE2LDAuMDIzLDMuODc0LDAuNjA4LDUuMTQxLDEuNzU4YzEuMjc4LDEuMTYsMS45MjksMi43NjQsMS45NSw0LjgxMQoJCQljMCwxLjE0Mi0wLjEzNywyLjExMS0wLjQxLDIuOTExYy0wLjMwOSwwLjg0NS0wLjczMSwxLjU5My0xLjI2OCwyLjI0M2MtMC40OTIsMC42NS0xLjA2OCwxLjMxOC0xLjczLDIuMDAyCgkJCWMtMC42NSwwLjY5Ny0xLjMxMywxLjQ3OS0xLjk4NywyLjM0NmMtMC4yMzksMC4zNzctMC40MjksMC43NzctMC41NjUsMS4xOTljLTAuMTYsMC45NTktMC4yMTcsMS45NTEtMC4xNzEsMi45NzkKCQkJQzI2LjU4OSwzMi4yMTgsMjMuNTc4LDMyLjIxOCwyMy41NzgsMzIuMjE4eiBNMjMuNTc4LDM4LjIydi0zLjQ4NGgzLjA3NnYzLjQ4NEgyMy41Nzh6Ii8+Cgk8L2c+Cjwvc3ZnPgo=);
  --jp-icon-markdown: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8cGF0aCBjbGFzcz0ianAtaWNvbi1jb250cmFzdDAganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjN0IxRkEyIiBkPSJNNSAxNC45aDEybC02LjEgNnptOS40LTYuOGMwLTEuMy0uMS0yLjktLjEtNC41LS40IDEuNC0uOSAyLjktMS4zIDQuM2wtMS4zIDQuM2gtMkw4LjUgNy45Yy0uNC0xLjMtLjctMi45LTEtNC4zLS4xIDEuNi0uMSAzLjItLjIgNC42TDcgMTIuNEg0LjhsLjctMTFoMy4zTDEwIDVjLjQgMS4yLjcgMi43IDEgMy45LjMtMS4yLjctMi42IDEtMy45bDEuMi0zLjdoMy4zbC42IDExaC0yLjRsLS4zLTQuMnoiLz4KPC9zdmc+Cg==);
  --jp-icon-new-folder: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTIwIDZoLThsLTItMkg0Yy0xLjExIDAtMS45OS44OS0xLjk5IDJMMiAxOGMwIDEuMTEuODkgMiAyIDJoMTZjMS4xMSAwIDItLjg5IDItMlY4YzAtMS4xMS0uODktMi0yLTJ6bS0xIDhoLTN2M2gtMnYtM2gtM3YtMmgzVjloMnYzaDN2MnoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-not-trusted: url(data:image/svg+xml;base64,PHN2ZyBmaWxsPSJub25lIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI1IDI1Ij4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uMiIgc3Ryb2tlPSIjMzMzMzMzIiBzdHJva2Utd2lkdGg9IjIiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDMgMykiIGQ9Ik0xLjg2MDk0IDExLjQ0MDlDMC44MjY0NDggOC43NzAyNyAwLjg2Mzc3OSA2LjA1NzY0IDEuMjQ5MDcgNC4xOTkzMkMyLjQ4MjA2IDMuOTMzNDcgNC4wODA2OCAzLjQwMzQ3IDUuNjAxMDIgMi44NDQ5QzcuMjM1NDkgMi4yNDQ0IDguODU2NjYgMS41ODE1IDkuOTg3NiAxLjA5NTM5QzExLjA1OTcgMS41ODM0MSAxMi42MDk0IDIuMjQ0NCAxNC4yMTggMi44NDMzOUMxNS43NTAzIDMuNDEzOTQgMTcuMzk5NSAzLjk1MjU4IDE4Ljc1MzkgNC4yMTM4NUMxOS4xMzY0IDYuMDcxNzcgMTkuMTcwOSA4Ljc3NzIyIDE4LjEzOSAxMS40NDA5QzE3LjAzMDMgMTQuMzAzMiAxNC42NjY4IDE3LjE4NDQgOS45OTk5OSAxOC45MzU0QzUuMzMzMTkgMTcuMTg0NCAyLjk2OTY4IDE0LjMwMzIgMS44NjA5NCAxMS40NDA5WiIvPgogICAgPHBhdGggY2xhc3M9ImpwLWljb24yIiBzdHJva2U9IiMzMzMzMzMiIHN0cm9rZS13aWR0aD0iMiIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoOS4zMTU5MiA5LjMyMDMxKSIgZD0iTTcuMzY4NDIgMEwwIDcuMzY0NzkiLz4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uMiIgc3Ryb2tlPSIjMzMzMzMzIiBzdHJva2Utd2lkdGg9IjIiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDkuMzE1OTIgMTYuNjgzNikgc2NhbGUoMSAtMSkiIGQ9Ik03LjM2ODQyIDBMMCA3LjM2NDc5Ii8+Cjwvc3ZnPgo=);
  --jp-icon-notebook: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8ZyBjbGFzcz0ianAtaWNvbi13YXJuMCBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiNFRjZDMDAiPgogICAgPHBhdGggZD0iTTE4LjcgMy4zdjE1LjRIMy4zVjMuM2gxNS40bTEuNS0xLjVIMS44djE4LjNoMTguM2wuMS0xOC4zeiIvPgogICAgPHBhdGggZD0iTTE2LjUgMTYuNWwtNS40LTQuMy01LjYgNC4zdi0xMWgxMXoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-numbering: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjIiIGhlaWdodD0iMjIiIHZpZXdCb3g9IjAgMCAyOCAyOCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CgkJPHBhdGggZD0iTTQgMTlINlYxOS41SDVWMjAuNUg2VjIxSDRWMjJIN1YxOEg0VjE5Wk01IDEwSDZWNkg0VjdINVYxMFpNNCAxM0g1LjhMNCAxNS4xVjE2SDdWMTVINS4yTDcgMTIuOVYxMkg0VjEzWk05IDdWOUgyM1Y3SDlaTTkgMjFIMjNWMTlIOVYyMVpNOSAxNUgyM1YxM0g5VjE1WiIvPgoJPC9nPgo8L3N2Zz4K);
  --jp-icon-offline-bolt: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCIgd2lkdGg9IjE2Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTEyIDIuMDJjLTUuNTEgMC05Ljk4IDQuNDctOS45OCA5Ljk4czQuNDcgOS45OCA5Ljk4IDkuOTggOS45OC00LjQ3IDkuOTgtOS45OFMxNy41MSAyLjAyIDEyIDIuMDJ6TTExLjQ4IDIwdi02LjI2SDhMMTMgNHY2LjI2aDMuMzVMMTEuNDggMjB6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-palette: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTE4IDEzVjIwSDRWNkg5LjAyQzkuMDcgNS4yOSA5LjI0IDQuNjIgOS41IDRINEMyLjkgNCAyIDQuOSAyIDZWMjBDMiAyMS4xIDIuOSAyMiA0IDIySDE4QzE5LjEgMjIgMjAgMjEuMSAyMCAyMFYxNUwxOCAxM1pNMTkuMyA4Ljg5QzE5Ljc0IDguMTkgMjAgNy4zOCAyMCA2LjVDMjAgNC4wMSAxNy45OSAyIDE1LjUgMkMxMy4wMSAyIDExIDQuMDEgMTEgNi41QzExIDguOTkgMTMuMDEgMTEgMTUuNDkgMTFDMTYuMzcgMTEgMTcuMTkgMTAuNzQgMTcuODggMTAuM0wyMSAxMy40MkwyMi40MiAxMkwxOS4zIDguODlaTTE1LjUgOUMxNC4xMiA5IDEzIDcuODggMTMgNi41QzEzIDUuMTIgMTQuMTIgNCAxNS41IDRDMTYuODggNCAxOCA1LjEyIDE4IDYuNUMxOCA3Ljg4IDE2Ljg4IDkgMTUuNSA5WiIvPgogICAgPHBhdGggZmlsbC1ydWxlPSJldmVub2RkIiBjbGlwLXJ1bGU9ImV2ZW5vZGQiIGQ9Ik00IDZIOS4wMTg5NEM5LjAwNjM5IDYuMTY1MDIgOSA2LjMzMTc2IDkgNi41QzkgOC44MTU3NyAxMC4yMTEgMTAuODQ4NyAxMi4wMzQzIDEySDlWMTRIMTZWMTIuOTgxMUMxNi41NzAzIDEyLjkzNzcgMTcuMTIgMTIuODIwNyAxNy42Mzk2IDEyLjYzOTZMMTggMTNWMjBINFY2Wk04IDhINlYxMEg4VjhaTTYgMTJIOFYxNEg2VjEyWk04IDE2SDZWMThIOFYxNlpNOSAxNkgxNlYxOEg5VjE2WiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-paste: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTE5IDJoLTQuMThDMTQuNC44NCAxMy4zIDAgMTIgMGMtMS4zIDAtMi40Ljg0LTIuODIgMkg1Yy0xLjEgMC0yIC45LTIgMnYxNmMwIDEuMS45IDIgMiAyaDE0YzEuMSAwIDItLjkgMi0yVjRjMC0xLjEtLjktMi0yLTJ6bS03IDBjLjU1IDAgMSAuNDUgMSAxcy0uNDUgMS0xIDEtMS0uNDUtMS0xIC40NS0xIDEtMXptNyAxOEg1VjRoMnYzaDEwVjRoMnYxNnoiLz4KICAgIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-pdf: url(data:image/svg+xml;base64,PHN2ZwogICB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyMiAyMiIgd2lkdGg9IjE2Ij4KICAgIDxwYXRoIHRyYW5zZm9ybT0icm90YXRlKDQ1KSIgY2xhc3M9ImpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iI0ZGMkEyQSIKICAgICAgIGQ9Im0gMjIuMzQ0MzY5LC0zLjAxNjM2NDIgaCA1LjYzODYwNCB2IDEuNTc5MjQzMyBoIC0zLjU0OTIyNyB2IDEuNTA4NjkyOTkgaCAzLjMzNzU3NiBWIDEuNjUwODE1NCBoIC0zLjMzNzU3NiB2IDMuNDM1MjYxMyBoIC0yLjA4OTM3NyB6IG0gLTcuMTM2NDQ0LDEuNTc5MjQzMyB2IDQuOTQzOTU0MyBoIDAuNzQ4OTIgcSAxLjI4MDc2MSwwIDEuOTUzNzAzLC0wLjYzNDk1MzUgMC42NzgzNjksLTAuNjM0OTUzNSAwLjY3ODM2OSwtMS44NDUxNjQxIDAsLTEuMjA0NzgzNTUgLTAuNjcyOTQyLC0xLjgzNDMxMDExIC0wLjY3Mjk0MiwtMC42Mjk1MjY1OSAtMS45NTkxMywtMC42Mjk1MjY1OSB6IG0gLTIuMDg5Mzc3LC0xLjU3OTI0MzMgaCAyLjIwMzM0MyBxIDEuODQ1MTY0LDAgMi43NDYwMzksMC4yNjU5MjA3IDAuOTA2MzAxLDAuMjYwNDkzNyAxLjU1MjEwOCwwLjg5MDAyMDMgMC41Njk4MywwLjU0ODEyMjMgMC44NDY2MDUsMS4yNjQ0ODAwNiAwLjI3Njc3NCwwLjcxNjM1NzgxIDAuMjc2Nzc0LDEuNjIyNjU4OTQgMCwwLjkxNzE1NTEgLTAuMjc2Nzc0LDEuNjM4OTM5OSAtMC4yNzY3NzUsMC43MTYzNTc4IC0wLjg0NjYwNSwxLjI2NDQ4IC0wLjY1MTIzNCwwLjYyOTUyNjYgLTEuNTYyOTYyLDAuODk1NDQ3MyAtMC45MTE3MjgsMC4yNjA0OTM3IC0yLjczNTE4NSwwLjI2MDQ5MzcgaCAtMi4yMDMzNDMgeiBtIC04LjE0NTg1NjUsMCBoIDMuNDY3ODIzIHEgMS41NDY2ODE2LDAgMi4zNzE1Nzg1LDAuNjg5MjIzIDAuODMwMzI0LDAuNjgzNzk2MSAwLjgzMDMyNCwxLjk1MzcwMzE0IDAsMS4yNzUzMzM5NyAtMC44MzAzMjQsMS45NjQ1NTcwNiBRIDkuOTg3MTk2MSwyLjI3NDkxNSA4LjQ0MDUxNDUsMi4yNzQ5MTUgSCA3LjA2MjA2ODQgViA1LjA4NjA3NjcgSCA0Ljk3MjY5MTUgWiBtIDIuMDg5Mzc2OSwxLjUxNDExOTkgdiAyLjI2MzAzOTQzIGggMS4xNTU5NDEgcSAwLjYwNzgxODgsMCAwLjkzODg2MjksLTAuMjkzMDU1NDcgMC4zMzEwNDQxLC0wLjI5ODQ4MjQxIDAuMzMxMDQ0MSwtMC44NDExNzc3MiAwLC0wLjU0MjY5NTMxIC0wLjMzMTA0NDEsLTAuODM1NzUwNzQgLTAuMzMxMDQ0MSwtMC4yOTMwNTU1IC0wLjkzODg2MjksLTAuMjkzMDU1NSB6IgovPgo8L3N2Zz4K);
  --jp-icon-python: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8ZyBjbGFzcz0ianAtaWNvbi1icmFuZDAganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjMEQ0N0ExIj4KICAgIDxwYXRoIGQ9Ik0xMS4xIDYuOVY1LjhINi45YzAtLjUgMC0xLjMuMi0xLjYuNC0uNy44LTEuMSAxLjctMS40IDEuNy0uMyAyLjUtLjMgMy45LS4xIDEgLjEgMS45LjkgMS45IDEuOXY0LjJjMCAuNS0uOSAxLjYtMiAxLjZIOC44Yy0xLjUgMC0yLjQgMS40LTIuNCAyLjh2Mi4ySDQuN0MzLjUgMTUuMSAzIDE0IDMgMTMuMVY5Yy0uMS0xIC42LTIgMS44LTIgMS41LS4xIDYuMy0uMSA2LjMtLjF6Ii8+CiAgICA8cGF0aCBkPSJNMTAuOSAxNS4xdjEuMWg0LjJjMCAuNSAwIDEuMy0uMiAxLjYtLjQuNy0uOCAxLjEtMS43IDEuNC0xLjcuMy0yLjUuMy0zLjkuMS0xLS4xLTEuOS0uOS0xLjktMS45di00LjJjMC0uNS45LTEuNiAyLTEuNmgzLjhjMS41IDAgMi40LTEuNCAyLjQtMi44VjYuNmgxLjdDMTguNSA2LjkgMTkgOCAxOSA4LjlWMTNjMCAxLS43IDIuMS0xLjkgMi4xaC02LjJ6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-r-kernel: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8cGF0aCBjbGFzcz0ianAtaWNvbi1jb250cmFzdDMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjMjE5NkYzIiBkPSJNNC40IDIuNWMxLjItLjEgMi45LS4zIDQuOS0uMyAyLjUgMCA0LjEuNCA1LjIgMS4zIDEgLjcgMS41IDEuOSAxLjUgMy41IDAgMi0xLjQgMy41LTIuOSA0LjEgMS4yLjQgMS43IDEuNiAyLjIgMyAuNiAxLjkgMSAzLjkgMS4zIDQuNmgtMy44Yy0uMy0uNC0uOC0xLjctMS4yLTMuN3MtMS4yLTIuNi0yLjYtMi42aC0uOXY2LjRINC40VjIuNXptMy43IDYuOWgxLjRjMS45IDAgMi45LS45IDIuOS0yLjNzLTEtMi4zLTIuOC0yLjNjLS43IDAtMS4zIDAtMS42LjJ2NC41aC4xdi0uMXoiLz4KPC9zdmc+Cg==);
  --jp-icon-react: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMTUwIDE1MCA1NDEuOSAyOTUuMyI+CiAgPGcgY2xhc3M9ImpwLWljb24tYnJhbmQyIGpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iIzYxREFGQiI+CiAgICA8cGF0aCBkPSJNNjY2LjMgMjk2LjVjMC0zMi41LTQwLjctNjMuMy0xMDMuMS04Mi40IDE0LjQtNjMuNiA4LTExNC4yLTIwLjItMTMwLjQtNi41LTMuOC0xNC4xLTUuNi0yMi40LTUuNnYyMi4zYzQuNiAwIDguMy45IDExLjQgMi42IDEzLjYgNy44IDE5LjUgMzcuNSAxNC45IDc1LjctMS4xIDkuNC0yLjkgMTkuMy01LjEgMjkuNC0xOS42LTQuOC00MS04LjUtNjMuNS0xMC45LTEzLjUtMTguNS0yNy41LTM1LjMtNDEuNi01MCAzMi42LTMwLjMgNjMuMi00Ni45IDg0LTQ2LjlWNzhjLTI3LjUgMC02My41IDE5LjYtOTkuOSA1My42LTM2LjQtMzMuOC03Mi40LTUzLjItOTkuOS01My4ydjIyLjNjMjAuNyAwIDUxLjQgMTYuNSA4NCA0Ni42LTE0IDE0LjctMjggMzEuNC00MS4zIDQ5LjktMjIuNiAyLjQtNDQgNi4xLTYzLjYgMTEtMi4zLTEwLTQtMTkuNy01LjItMjktNC43LTM4LjIgMS4xLTY3LjkgMTQuNi03NS44IDMtMS44IDYuOS0yLjYgMTEuNS0yLjZWNzguNWMtOC40IDAtMTYgMS44LTIyLjYgNS42LTI4LjEgMTYuMi0zNC40IDY2LjctMTkuOSAxMzAuMS02Mi4yIDE5LjItMTAyLjcgNDkuOS0xMDIuNyA4Mi4zIDAgMzIuNSA0MC43IDYzLjMgMTAzLjEgODIuNC0xNC40IDYzLjYtOCAxMTQuMiAyMC4yIDEzMC40IDYuNSAzLjggMTQuMSA1LjYgMjIuNSA1LjYgMjcuNSAwIDYzLjUtMTkuNiA5OS45LTUzLjYgMzYuNCAzMy44IDcyLjQgNTMuMiA5OS45IDUzLjIgOC40IDAgMTYtMS44IDIyLjYtNS42IDI4LjEtMTYuMiAzNC40LTY2LjcgMTkuOS0xMzAuMSA2Mi0xOS4xIDEwMi41LTQ5LjkgMTAyLjUtODIuM3ptLTEzMC4yLTY2LjdjLTMuNyAxMi45LTguMyAyNi4yLTEzLjUgMzkuNS00LjEtOC04LjQtMTYtMTMuMS0yNC00LjYtOC05LjUtMTUuOC0xNC40LTIzLjQgMTQuMiAyLjEgMjcuOSA0LjcgNDEgNy45em0tNDUuOCAxMDYuNWMtNy44IDEzLjUtMTUuOCAyNi4zLTI0LjEgMzguMi0xNC45IDEuMy0zMCAyLTQ1LjIgMi0xNS4xIDAtMzAuMi0uNy00NS0xLjktOC4zLTExLjktMTYuNC0yNC42LTI0LjItMzgtNy42LTEzLjEtMTQuNS0yNi40LTIwLjgtMzkuOCA2LjItMTMuNCAxMy4yLTI2LjggMjAuNy0zOS45IDcuOC0xMy41IDE1LjgtMjYuMyAyNC4xLTM4LjIgMTQuOS0xLjMgMzAtMiA0NS4yLTIgMTUuMSAwIDMwLjIuNyA0NSAxLjkgOC4zIDExLjkgMTYuNCAyNC42IDI0LjIgMzggNy42IDEzLjEgMTQuNSAyNi40IDIwLjggMzkuOC02LjMgMTMuNC0xMy4yIDI2LjgtMjAuNyAzOS45em0zMi4zLTEzYzUuNCAxMy40IDEwIDI2LjggMTMuOCAzOS44LTEzLjEgMy4yLTI2LjkgNS45LTQxLjIgOCA0LjktNy43IDkuOC0xNS42IDE0LjQtMjMuNyA0LjYtOCA4LjktMTYuMSAxMy0yNC4xek00MjEuMiA0MzBjLTkuMy05LjYtMTguNi0yMC4zLTI3LjgtMzIgOSAuNCAxOC4yLjcgMjcuNS43IDkuNCAwIDE4LjctLjIgMjcuOC0uNy05IDExLjctMTguMyAyMi40LTI3LjUgMzJ6bS03NC40LTU4LjljLTE0LjItMi4xLTI3LjktNC43LTQxLTcuOSAzLjctMTIuOSA4LjMtMjYuMiAxMy41LTM5LjUgNC4xIDggOC40IDE2IDEzLjEgMjQgNC43IDggOS41IDE1LjggMTQuNCAyMy40ek00MjAuNyAxNjNjOS4zIDkuNiAxOC42IDIwLjMgMjcuOCAzMi05LS40LTE4LjItLjctMjcuNS0uNy05LjQgMC0xOC43LjItMjcuOC43IDktMTEuNyAxOC4zLTIyLjQgMjcuNS0zMnptLTc0IDU4LjljLTQuOSA3LjctOS44IDE1LjYtMTQuNCAyMy43LTQuNiA4LTguOSAxNi0xMyAyNC01LjQtMTMuNC0xMC0yNi44LTEzLjgtMzkuOCAxMy4xLTMuMSAyNi45LTUuOCA0MS4yLTcuOXptLTkwLjUgMTI1LjJjLTM1LjQtMTUuMS01OC4zLTM0LjktNTguMy01MC42IDAtMTUuNyAyMi45LTM1LjYgNTguMy01MC42IDguNi0zLjcgMTgtNyAyNy43LTEwLjEgNS43IDE5LjYgMTMuMiA0MCAyMi41IDYwLjktOS4yIDIwLjgtMTYuNiA0MS4xLTIyLjIgNjAuNi05LjktMy4xLTE5LjMtNi41LTI4LTEwLjJ6TTMxMCA0OTBjLTEzLjYtNy44LTE5LjUtMzcuNS0xNC45LTc1LjcgMS4xLTkuNCAyLjktMTkuMyA1LjEtMjkuNCAxOS42IDQuOCA0MSA4LjUgNjMuNSAxMC45IDEzLjUgMTguNSAyNy41IDM1LjMgNDEuNiA1MC0zMi42IDMwLjMtNjMuMiA0Ni45LTg0IDQ2LjktNC41LS4xLTguMy0xLTExLjMtMi43em0yMzcuMi03Ni4yYzQuNyAzOC4yLTEuMSA2Ny45LTE0LjYgNzUuOC0zIDEuOC02LjkgMi42LTExLjUgMi42LTIwLjcgMC01MS40LTE2LjUtODQtNDYuNiAxNC0xNC43IDI4LTMxLjQgNDEuMy00OS45IDIyLjYtMi40IDQ0LTYuMSA2My42LTExIDIuMyAxMC4xIDQuMSAxOS44IDUuMiAyOS4xem0zOC41LTY2LjdjLTguNiAzLjctMTggNy0yNy43IDEwLjEtNS43LTE5LjYtMTMuMi00MC0yMi41LTYwLjkgOS4yLTIwLjggMTYuNi00MS4xIDIyLjItNjAuNiA5LjkgMy4xIDE5LjMgNi41IDI4LjEgMTAuMiAzNS40IDE1LjEgNTguMyAzNC45IDU4LjMgNTAuNi0uMSAxNS43LTIzIDM1LjYtNTguNCA1MC42ek0zMjAuOCA3OC40eiIvPgogICAgPGNpcmNsZSBjeD0iNDIwLjkiIGN5PSIyOTYuNSIgcj0iNDUuNyIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-redo: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIGhlaWdodD0iMjQiIHZpZXdCb3g9IjAgMCAyNCAyNCIgd2lkdGg9IjE2Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgICA8cGF0aCBkPSJNMCAwaDI0djI0SDB6IiBmaWxsPSJub25lIi8+PHBhdGggZD0iTTE4LjQgMTAuNkMxNi41NSA4Ljk5IDE0LjE1IDggMTEuNSA4Yy00LjY1IDAtOC41OCAzLjAzLTkuOTYgNy4yMkwzLjkgMTZjMS4wNS0zLjE5IDQuMDUtNS41IDcuNi01LjUgMS45NSAwIDMuNzMuNzIgNS4xMiAxLjg4TDEzIDE2aDlWN2wtMy42IDMuNnoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-refresh: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTkgMTMuNWMtMi40OSAwLTQuNS0yLjAxLTQuNS00LjVTNi41MSA0LjUgOSA0LjVjMS4yNCAwIDIuMzYuNTIgMy4xNyAxLjMzTDEwIDhoNVYzbC0xLjc2IDEuNzZDMTIuMTUgMy42OCAxMC42NiAzIDkgMyA1LjY5IDMgMy4wMSA1LjY5IDMuMDEgOVM1LjY5IDE1IDkgMTVjMi45NyAwIDUuNDMtMi4xNiA1LjktNWgtMS41MmMtLjQ2IDItMi4yNCAzLjUtNC4zOCAzLjV6Ii8+CiAgICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-regex: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIwIDIwIj4KICA8ZyBjbGFzcz0ianAtaWNvbjIiIGZpbGw9IiM0MTQxNDEiPgogICAgPHJlY3QgeD0iMiIgeT0iMiIgd2lkdGg9IjE2IiBoZWlnaHQ9IjE2Ii8+CiAgPC9nPgoKICA8ZyBjbGFzcz0ianAtaWNvbi1hY2NlbnQyIiBmaWxsPSIjRkZGIj4KICAgIDxjaXJjbGUgY2xhc3M9InN0MiIgY3g9IjUuNSIgY3k9IjE0LjUiIHI9IjEuNSIvPgogICAgPHJlY3QgeD0iMTIiIHk9IjQiIGNsYXNzPSJzdDIiIHdpZHRoPSIxIiBoZWlnaHQ9IjgiLz4KICAgIDxyZWN0IHg9IjguNSIgeT0iNy41IiB0cmFuc2Zvcm09Im1hdHJpeCgwLjg2NiAtMC41IDAuNSAwLjg2NiAtMi4zMjU1IDcuMzIxOSkiIGNsYXNzPSJzdDIiIHdpZHRoPSI4IiBoZWlnaHQ9IjEiLz4KICAgIDxyZWN0IHg9IjEyIiB5PSI0IiB0cmFuc2Zvcm09Im1hdHJpeCgwLjUgLTAuODY2IDAuODY2IDAuNSAtMC42Nzc5IDE0LjgyNTIpIiBjbGFzcz0ic3QyIiB3aWR0aD0iMSIgaGVpZ2h0PSI4Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-run: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTggNXYxNGwxMS03eiIvPgogICAgPC9nPgo8L3N2Zz4K);
  --jp-icon-running: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDUxMiA1MTIiPgogIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICA8cGF0aCBkPSJNMjU2IDhDMTE5IDggOCAxMTkgOCAyNTZzMTExIDI0OCAyNDggMjQ4IDI0OC0xMTEgMjQ4LTI0OFMzOTMgOCAyNTYgOHptOTYgMzI4YzAgOC44LTcuMiAxNi0xNiAxNkgxNzZjLTguOCAwLTE2LTcuMi0xNi0xNlYxNzZjMC04LjggNy4yLTE2IDE2LTE2aDE2MGM4LjggMCAxNiA3LjIgMTYgMTZ2MTYweiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-save: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTE3IDNINWMtMS4xMSAwLTIgLjktMiAydjE0YzAgMS4xLjg5IDIgMiAyaDE0YzEuMSAwIDItLjkgMi0yVjdsLTQtNHptLTUgMTZjLTEuNjYgMC0zLTEuMzQtMy0zczEuMzQtMyAzLTMgMyAxLjM0IDMgMy0xLjM0IDMtMyAzem0zLTEwSDVWNWgxMHY0eiIvPgogICAgPC9nPgo8L3N2Zz4K);
  --jp-icon-search: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMTggMTgiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTEyLjEsMTAuOWgtMC43bC0wLjItMC4yYzAuOC0wLjksMS4zLTIuMiwxLjMtMy41YzAtMy0yLjQtNS40LTUuNC01LjRTMS44LDQuMiwxLjgsNy4xczIuNCw1LjQsNS40LDUuNCBjMS4zLDAsMi41LTAuNSwzLjUtMS4zbDAuMiwwLjJ2MC43bDQuMSw0LjFsMS4yLTEuMkwxMi4xLDEwLjl6IE03LjEsMTAuOWMtMi4xLDAtMy43LTEuNy0zLjctMy43czEuNy0zLjcsMy43LTMuN3MzLjcsMS43LDMuNywzLjcgUzkuMiwxMC45LDcuMSwxMC45eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-settings: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMTkuNDMgMTIuOThjLjA0LS4zMi4wNy0uNjQuMDctLjk4cy0uMDMtLjY2LS4wNy0uOThsMi4xMS0xLjY1Yy4xOS0uMTUuMjQtLjQyLjEyLS42NGwtMi0zLjQ2Yy0uMTItLjIyLS4zOS0uMy0uNjEtLjIybC0yLjQ5IDFjLS41Mi0uNC0xLjA4LS43My0xLjY5LS45OGwtLjM4LTIuNjVBLjQ4OC40ODggMCAwMDE0IDJoLTRjLS4yNSAwLS40Ni4xOC0uNDkuNDJsLS4zOCAyLjY1Yy0uNjEuMjUtMS4xNy41OS0xLjY5Ljk4bC0yLjQ5LTFjLS4yMy0uMDktLjQ5IDAtLjYxLjIybC0yIDMuNDZjLS4xMy4yMi0uMDcuNDkuMTIuNjRsMi4xMSAxLjY1Yy0uMDQuMzItLjA3LjY1LS4wNy45OHMuMDMuNjYuMDcuOThsLTIuMTEgMS42NWMtLjE5LjE1LS4yNC40Mi0uMTIuNjRsMiAzLjQ2Yy4xMi4yMi4zOS4zLjYxLjIybDIuNDktMWMuNTIuNCAxLjA4LjczIDEuNjkuOThsLjM4IDIuNjVjLjAzLjI0LjI0LjQyLjQ5LjQyaDRjLjI1IDAgLjQ2LS4xOC40OS0uNDJsLjM4LTIuNjVjLjYxLS4yNSAxLjE3LS41OSAxLjY5LS45OGwyLjQ5IDFjLjIzLjA5LjQ5IDAgLjYxLS4yMmwyLTMuNDZjLjEyLS4yMi4wNy0uNDktLjEyLS42NGwtMi4xMS0xLjY1ek0xMiAxNS41Yy0xLjkzIDAtMy41LTEuNTctMy41LTMuNXMxLjU3LTMuNSAzLjUtMy41IDMuNSAxLjU3IDMuNSAzLjUtMS41NyAzLjUtMy41IDMuNXoiLz4KPC9zdmc+Cg==);
  --jp-icon-spreadsheet: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8cGF0aCBjbGFzcz0ianAtaWNvbi1jb250cmFzdDEganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNENBRjUwIiBkPSJNMi4yIDIuMnYxNy42aDE3LjZWMi4ySDIuMnptMTUuNCA3LjdoLTUuNVY0LjRoNS41djUuNXpNOS45IDQuNHY1LjVINC40VjQuNGg1LjV6bS01LjUgNy43aDUuNXY1LjVINC40di01LjV6bTcuNyA1LjV2LTUuNWg1LjV2NS41aC01LjV6Ii8+Cjwvc3ZnPgo=);
  --jp-icon-stop: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTAgMGgyNHYyNEgweiIgZmlsbD0ibm9uZSIvPgogICAgICAgIDxwYXRoIGQ9Ik02IDZoMTJ2MTJINnoiLz4KICAgIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-tab: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTIxIDNIM2MtMS4xIDAtMiAuOS0yIDJ2MTRjMCAxLjEuOSAyIDIgMmgxOGMxLjEgMCAyLS45IDItMlY1YzAtMS4xLS45LTItMi0yem0wIDE2SDNWNWgxMHY0aDh2MTB6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-table-rows: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTAgMGgyNHYyNEgweiIgZmlsbD0ibm9uZSIvPgogICAgICAgIDxwYXRoIGQ9Ik0yMSw4SDNWNGgxOFY4eiBNMjEsMTBIM3Y0aDE4VjEweiBNMjEsMTZIM3Y0aDE4VjE2eiIvPgogICAgPC9nPgo8L3N2Zz4=);
  --jp-icon-tag: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjgiIGhlaWdodD0iMjgiIHZpZXdCb3g9IjAgMCA0MyAyOCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CgkJPHBhdGggZD0iTTI4LjgzMzIgMTIuMzM0TDMyLjk5OTggMTYuNTAwN0wzNy4xNjY1IDEyLjMzNEgyOC44MzMyWiIvPgoJCTxwYXRoIGQ9Ik0xNi4yMDk1IDIxLjYxMDRDMTUuNjg3MyAyMi4xMjk5IDE0Ljg0NDMgMjIuMTI5OSAxNC4zMjQ4IDIxLjYxMDRMNi45ODI5IDE0LjcyNDVDNi41NzI0IDE0LjMzOTQgNi4wODMxMyAxMy42MDk4IDYuMDQ3ODYgMTMuMDQ4MkM1Ljk1MzQ3IDExLjUyODggNi4wMjAwMiA4LjYxOTQ0IDYuMDY2MjEgNy4wNzY5NUM2LjA4MjgxIDYuNTE0NzcgNi41NTU0OCA2LjA0MzQ3IDcuMTE4MDQgNi4wMzA1NUM5LjA4ODYzIDUuOTg0NzMgMTMuMjYzOCA1LjkzNTc5IDEzLjY1MTggNi4zMjQyNUwyMS43MzY5IDEzLjYzOUMyMi4yNTYgMTQuMTU4NSAyMS43ODUxIDE1LjQ3MjQgMjEuMjYyIDE1Ljk5NDZMMTYuMjA5NSAyMS42MTA0Wk05Ljc3NTg1IDguMjY1QzkuMzM1NTEgNy44MjU2NiA4LjYyMzUxIDcuODI1NjYgOC4xODI4IDguMjY1QzcuNzQzNDYgOC43MDU3MSA3Ljc0MzQ2IDkuNDE3MzMgOC4xODI4IDkuODU2NjdDOC42MjM4MiAxMC4yOTY0IDkuMzM1ODIgMTAuMjk2NCA5Ljc3NTg1IDkuODU2NjdDMTAuMjE1NiA5LjQxNzMzIDEwLjIxNTYgOC43MDUzMyA5Ljc3NTg1IDguMjY1WiIvPgoJPC9nPgo8L3N2Zz4K);
  --jp-icon-terminal: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0IiA+CiAgICA8cmVjdCBjbGFzcz0ianAtaWNvbjIganAtaWNvbi1zZWxlY3RhYmxlIiB3aWR0aD0iMjAiIGhlaWdodD0iMjAiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDIgMikiIGZpbGw9IiMzMzMzMzMiLz4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uLWFjY2VudDIganAtaWNvbi1zZWxlY3RhYmxlLWludmVyc2UiIGQ9Ik01LjA1NjY0IDguNzYxNzJDNS4wNTY2NCA4LjU5NzY2IDUuMDMxMjUgOC40NTMxMiA0Ljk4MDQ3IDguMzI4MTJDNC45MzM1OSA4LjE5OTIyIDQuODU1NDcgOC4wODIwMyA0Ljc0NjA5IDcuOTc2NTZDNC42NDA2MiA3Ljg3MTA5IDQuNSA3Ljc3NTM5IDQuMzI0MjIgNy42ODk0NUM0LjE1MjM0IDcuNTk5NjEgMy45NDMzNiA3LjUxMTcyIDMuNjk3MjcgNy40MjU3OEMzLjMwMjczIDcuMjg1MTYgMi45NDMzNiA3LjEzNjcyIDIuNjE5MTQgNi45ODA0N0MyLjI5NDkyIDYuODI0MjIgMi4wMTc1OCA2LjY0MjU4IDEuNzg3MTEgNi40MzU1NUMxLjU2MDU1IDYuMjI4NTIgMS4zODQ3NyA1Ljk4ODI4IDEuMjU5NzcgNS43MTQ4NEMxLjEzNDc3IDUuNDM3NSAxLjA3MjI3IDUuMTA5MzggMS4wNzIyNyA0LjczMDQ3QzEuMDcyMjcgNC4zOTg0NCAxLjEyODkxIDQuMDk1NyAxLjI0MjE5IDMuODIyMjdDMS4zNTU0NyAzLjU0NDkyIDEuNTE1NjIgMy4zMDQ2OSAxLjcyMjY2IDMuMTAxNTZDMS45Mjk2OSAyLjg5ODQ0IDIuMTc5NjkgMi43MzQzNyAyLjQ3MjY2IDIuNjA5MzhDMi43NjU2MiAyLjQ4NDM4IDMuMDkxOCAyLjQwNDMgMy40NTExNyAyLjM2OTE0VjEuMTA5MzhINC4zODg2N1YyLjM4MDg2QzQuNzQwMjMgMi40Mjc3MyA1LjA1NjY0IDIuNTIzNDQgNS4zMzc4OSAyLjY2Nzk3QzUuNjE5MTQgMi44MTI1IDUuODU3NDIgMy4wMDE5NSA2LjA1MjczIDMuMjM2MzNDNi4yNTE5NSAzLjQ2NjggNi40MDQzIDMuNzQwMjMgNi41MDk3NyA0LjA1NjY0QzYuNjE5MTQgNC4zNjkxNCA2LjY3MzgzIDQuNzIwNyA2LjY3MzgzIDUuMTExMzNINS4wNDQ5MkM1LjA0NDkyIDQuNjM4NjcgNC45Mzc1IDQuMjgxMjUgNC43MjI2NiA0LjAzOTA2QzQuNTA3ODEgMy43OTI5NyA0LjIxNjggMy42Njk5MiAzLjg0OTYxIDMuNjY5OTJDMy42NTAzOSAzLjY2OTkyIDMuNDc2NTYgMy42OTcyNyAzLjMyODEyIDMuNzUxOTVDMy4xODM1OSAzLjgwMjczIDMuMDY0NDUgMy44NzY5NSAyLjk3MDcgMy45NzQ2MUMyLjg3Njk1IDQuMDY4MzYgMi44MDY2NCA0LjE3OTY5IDIuNzU5NzcgNC4zMDg1OUMyLjcxNjggNC40Mzc1IDIuNjk1MzEgNC41NzgxMiAyLjY5NTMxIDQuNzMwNDdDMi42OTUzMSA0Ljg4MjgxIDIuNzE2OCA1LjAxOTUzIDIuNzU5NzcgNS4xNDA2MkMyLjgwNjY0IDUuMjU3ODEgMi44ODI4MSA1LjM2NzE5IDIuOTg4MjggNS40Njg3NUMzLjA5NzY2IDUuNTcwMzEgMy4yNDAyMyA1LjY2Nzk3IDMuNDE2MDIgNS43NjE3MkMzLjU5MTggNS44NTE1NiAzLjgxMDU1IDUuOTQzMzYgNC4wNzIyNyA2LjAzNzExQzQuNDY2OCA2LjE4NTU1IDQuODI0MjIgNi4zMzk4NCA1LjE0NDUzIDYuNUM1LjQ2NDg0IDYuNjU2MjUgNS43MzgyOCA2LjgzOTg0IDUuOTY0ODQgNy4wNTA3OEM2LjE5NTMxIDcuMjU3ODEgNi4zNzEwOSA3LjUgNi40OTIxOSA3Ljc3NzM0QzYuNjE3MTkgOC4wNTA3OCA2LjY3OTY5IDguMzc1IDYuNjc5NjkgOC43NUM2LjY3OTY5IDkuMDkzNzUgNi42MjMwNSA5LjQwNDMgNi41MDk3NyA5LjY4MTY0QzYuMzk2NDggOS45NTUwOCA2LjIzNDM4IDEwLjE5MTQgNi4wMjM0NCAxMC4zOTA2QzUuODEyNSAxMC41ODk4IDUuNTU4NTkgMTAuNzUgNS4yNjE3MiAxMC44NzExQzQuOTY0ODQgMTAuOTg4MyA0LjYzMjgxIDExLjA2NDUgNC4yNjU2MiAxMS4wOTk2VjEyLjI0OEgzLjMzMzk4VjExLjA5OTZDMy4wMDE5NSAxMS4wNjg0IDIuNjc5NjkgMTAuOTk2MSAyLjM2NzE5IDEwLjg4MjhDMi4wNTQ2OSAxMC43NjU2IDEuNzc3MzQgMTAuNTk3NyAxLjUzNTE2IDEwLjM3ODlDMS4yOTY4OCAxMC4xNjAyIDEuMTA1NDcgOS44ODQ3NyAwLjk2MDkzOCA5LjU1MjczQzAuODE2NDA2IDkuMjE2OCAwLjc0NDE0MSA4LjgxNDQ1IDAuNzQ0MTQxIDguMzQ1N0gyLjM3ODkxQzIuMzc4OTEgOC42MjY5NSAyLjQxOTkyIDguODYzMjggMi41MDE5NSA5LjA1NDY5QzIuNTgzOTggOS4yNDIxOSAyLjY4OTQ1IDkuMzkyNTggMi44MTgzNiA5LjUwNTg2QzIuOTUxMTcgOS42MTUyMyAzLjEwMTU2IDkuNjkzMzYgMy4yNjk1MyA5Ljc0MDIzQzMuNDM3NSA5Ljc4NzExIDMuNjA5MzggOS44MTA1NSAzLjc4NTE2IDkuODEwNTVDNC4yMDMxMiA5LjgxMDU1IDQuNTE5NTMgOS43MTI4OSA0LjczNDM4IDkuNTE3NThDNC45NDkyMiA5LjMyMjI3IDUuMDU2NjQgOS4wNzAzMSA1LjA1NjY0IDguNzYxNzJaTTEzLjQxOCAxMi4yNzE1SDguMDc0MjJWMTFIMTMuNDE4VjEyLjI3MTVaIiB0cmFuc2Zvcm09InRyYW5zbGF0ZSgzLjk1MjY0IDYpIiBmaWxsPSJ3aGl0ZSIvPgo8L3N2Zz4K);
  --jp-icon-text-editor: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMTUgMTVIM3YyaDEydi0yem0wLThIM3YyaDEyVjd6TTMgMTNoMTh2LTJIM3Yyem0wIDhoMTh2LTJIM3Yyek0zIDN2MmgxOFYzSDN6Ii8+Cjwvc3ZnPgo=);
  --jp-icon-toc: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIj4KICAgIDxwYXRoIGQ9Ik03LDVIMjFWN0g3VjVNNywxM1YxMUgyMVYxM0g3TTQsNC41QTEuNSwxLjUgMCAwLDEgNS41LDZBMS41LDEuNSAwIDAsMSA0LDcuNUExLjUsMS41IDAgMCwxIDIuNSw2QTEuNSwxLjUgMCAwLDEgNCw0LjVNNCwxMC41QTEuNSwxLjUgMCAwLDEgNS41LDEyQTEuNSwxLjUgMCAwLDEgNCwxMy41QTEuNSwxLjUgMCAwLDEgMi41LDEyQTEuNSwxLjUgMCAwLDEgNCwxMC41TTcsMTlWMTdIMjFWMTlIN000LDE2LjVBMS41LDEuNSAwIDAsMSA1LjUsMThBMS41LDEuNSAwIDAsMSA0LDE5LjVBMS41LDEuNSAwIDAsMSAyLjUsMThBMS41LDEuNSAwIDAsMSA0LDE2LjVaIiAvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-tree-view: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTAgMGgyNHYyNEgweiIgZmlsbD0ibm9uZSIvPgogICAgICAgIDxwYXRoIGQ9Ik0yMiAxMVYzaC03djNIOVYzSDJ2OGg3VjhoMnYxMGg0djNoN3YtOGgtN3YzaC0yVjhoMnYzeiIvPgogICAgPC9nPgo8L3N2Zz4=);
  --jp-icon-trusted: url(data:image/svg+xml;base64,PHN2ZyBmaWxsPSJub25lIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI1Ij4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uMiIgc3Ryb2tlPSIjMzMzMzMzIiBzdHJva2Utd2lkdGg9IjIiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDIgMykiIGQ9Ik0xLjg2MDk0IDExLjQ0MDlDMC44MjY0NDggOC43NzAyNyAwLjg2Mzc3OSA2LjA1NzY0IDEuMjQ5MDcgNC4xOTkzMkMyLjQ4MjA2IDMuOTMzNDcgNC4wODA2OCAzLjQwMzQ3IDUuNjAxMDIgMi44NDQ5QzcuMjM1NDkgMi4yNDQ0IDguODU2NjYgMS41ODE1IDkuOTg3NiAxLjA5NTM5QzExLjA1OTcgMS41ODM0MSAxMi42MDk0IDIuMjQ0NCAxNC4yMTggMi44NDMzOUMxNS43NTAzIDMuNDEzOTQgMTcuMzk5NSAzLjk1MjU4IDE4Ljc1MzkgNC4yMTM4NUMxOS4xMzY0IDYuMDcxNzcgMTkuMTcwOSA4Ljc3NzIyIDE4LjEzOSAxMS40NDA5QzE3LjAzMDMgMTQuMzAzMiAxNC42NjY4IDE3LjE4NDQgOS45OTk5OSAxOC45MzU0QzUuMzMzMiAxNy4xODQ0IDIuOTY5NjggMTQuMzAzMiAxLjg2MDk0IDExLjQ0MDlaIi8+CiAgICA8cGF0aCBjbGFzcz0ianAtaWNvbjIiIGZpbGw9IiMzMzMzMzMiIHN0cm9rZT0iIzMzMzMzMyIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoOCA5Ljg2NzE5KSIgZD0iTTIuODYwMTUgNC44NjUzNUwwLjcyNjU0OSAyLjk5OTU5TDAgMy42MzA0NUwyLjg2MDE1IDYuMTMxNTdMOCAwLjYzMDg3Mkw3LjI3ODU3IDBMMi44NjAxNSA0Ljg2NTM1WiIvPgo8L3N2Zz4K);
  --jp-icon-undo: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTEyLjUgOGMtMi42NSAwLTUuMDUuOTktNi45IDIuNkwyIDd2OWg5bC0zLjYyLTMuNjJjMS4zOS0xLjE2IDMuMTYtMS44OCA1LjEyLTEuODggMy41NCAwIDYuNTUgMi4zMSA3LjYgNS41bDIuMzctLjc4QzIxLjA4IDExLjAzIDE3LjE1IDggMTIuNSA4eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-vega: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8ZyBjbGFzcz0ianAtaWNvbjEganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjMjEyMTIxIj4KICAgIDxwYXRoIGQ9Ik0xMC42IDUuNGwyLjItMy4ySDIuMnY3LjNsNC02LjZ6Ii8+CiAgICA8cGF0aCBkPSJNMTUuOCAyLjJsLTQuNCA2LjZMNyA2LjNsLTQuOCA4djUuNWgxNy42VjIuMmgtNHptLTcgMTUuNEg1LjV2LTQuNGgzLjN2NC40em00LjQgMEg5LjhWOS44aDMuNHY3Ljh6bTQuNCAwaC0zLjRWNi41aDMuNHYxMS4xeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-yaml: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8ZyBjbGFzcz0ianAtaWNvbi1jb250cmFzdDIganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjRDgxQjYwIj4KICAgIDxwYXRoIGQ9Ik03LjIgMTguNnYtNS40TDMgNS42aDMuM2wxLjQgMy4xYy4zLjkuNiAxLjYgMSAyLjUuMy0uOC42LTEuNiAxLTIuNWwxLjQtMy4xaDMuNGwtNC40IDcuNnY1LjVsLTIuOS0uMXoiLz4KICAgIDxjaXJjbGUgY2xhc3M9InN0MCIgY3g9IjE3LjYiIGN5PSIxNi41IiByPSIyLjEiLz4KICAgIDxjaXJjbGUgY2xhc3M9InN0MCIgY3g9IjE3LjYiIGN5PSIxMSIgcj0iMi4xIi8+CiAgPC9nPgo8L3N2Zz4K);
}

/* Icon CSS class declarations */

.jp-AddIcon {
  background-image: var(--jp-icon-add);
}
.jp-BugIcon {
  background-image: var(--jp-icon-bug);
}
.jp-BuildIcon {
  background-image: var(--jp-icon-build);
}
.jp-CaretDownEmptyIcon {
  background-image: var(--jp-icon-caret-down-empty);
}
.jp-CaretDownEmptyThinIcon {
  background-image: var(--jp-icon-caret-down-empty-thin);
}
.jp-CaretDownIcon {
  background-image: var(--jp-icon-caret-down);
}
.jp-CaretLeftIcon {
  background-image: var(--jp-icon-caret-left);
}
.jp-CaretRightIcon {
  background-image: var(--jp-icon-caret-right);
}
.jp-CaretUpEmptyThinIcon {
  background-image: var(--jp-icon-caret-up-empty-thin);
}
.jp-CaretUpIcon {
  background-image: var(--jp-icon-caret-up);
}
.jp-CaseSensitiveIcon {
  background-image: var(--jp-icon-case-sensitive);
}
.jp-CheckIcon {
  background-image: var(--jp-icon-check);
}
.jp-CircleEmptyIcon {
  background-image: var(--jp-icon-circle-empty);
}
.jp-CircleIcon {
  background-image: var(--jp-icon-circle);
}
.jp-ClearIcon {
  background-image: var(--jp-icon-clear);
}
.jp-CloseIcon {
  background-image: var(--jp-icon-close);
}
.jp-CodeIcon {
  background-image: var(--jp-icon-code);
}
.jp-ConsoleIcon {
  background-image: var(--jp-icon-console);
}
.jp-CopyIcon {
  background-image: var(--jp-icon-copy);
}
.jp-CopyrightIcon {
  background-image: var(--jp-icon-copyright);
}
.jp-CutIcon {
  background-image: var(--jp-icon-cut);
}
.jp-DownloadIcon {
  background-image: var(--jp-icon-download);
}
.jp-EditIcon {
  background-image: var(--jp-icon-edit);
}
.jp-EllipsesIcon {
  background-image: var(--jp-icon-ellipses);
}
.jp-ExtensionIcon {
  background-image: var(--jp-icon-extension);
}
.jp-FastForwardIcon {
  background-image: var(--jp-icon-fast-forward);
}
.jp-FileIcon {
  background-image: var(--jp-icon-file);
}
.jp-FileUploadIcon {
  background-image: var(--jp-icon-file-upload);
}
.jp-FilterListIcon {
  background-image: var(--jp-icon-filter-list);
}
.jp-FolderIcon {
  background-image: var(--jp-icon-folder);
}
.jp-Html5Icon {
  background-image: var(--jp-icon-html5);
}
.jp-ImageIcon {
  background-image: var(--jp-icon-image);
}
.jp-InspectorIcon {
  background-image: var(--jp-icon-inspector);
}
.jp-JsonIcon {
  background-image: var(--jp-icon-json);
}
.jp-JuliaIcon {
  background-image: var(--jp-icon-julia);
}
.jp-JupyterFaviconIcon {
  background-image: var(--jp-icon-jupyter-favicon);
}
.jp-JupyterIcon {
  background-image: var(--jp-icon-jupyter);
}
.jp-JupyterlabWordmarkIcon {
  background-image: var(--jp-icon-jupyterlab-wordmark);
}
.jp-KernelIcon {
  background-image: var(--jp-icon-kernel);
}
.jp-KeyboardIcon {
  background-image: var(--jp-icon-keyboard);
}
.jp-LauncherIcon {
  background-image: var(--jp-icon-launcher);
}
.jp-LineFormIcon {
  background-image: var(--jp-icon-line-form);
}
.jp-LinkIcon {
  background-image: var(--jp-icon-link);
}
.jp-ListIcon {
  background-image: var(--jp-icon-list);
}
.jp-ListingsInfoIcon {
  background-image: var(--jp-icon-listings-info);
}
.jp-MarkdownIcon {
  background-image: var(--jp-icon-markdown);
}
.jp-NewFolderIcon {
  background-image: var(--jp-icon-new-folder);
}
.jp-NotTrustedIcon {
  background-image: var(--jp-icon-not-trusted);
}
.jp-NotebookIcon {
  background-image: var(--jp-icon-notebook);
}
.jp-NumberingIcon {
  background-image: var(--jp-icon-numbering);
}
.jp-OfflineBoltIcon {
  background-image: var(--jp-icon-offline-bolt);
}
.jp-PaletteIcon {
  background-image: var(--jp-icon-palette);
}
.jp-PasteIcon {
  background-image: var(--jp-icon-paste);
}
.jp-PdfIcon {
  background-image: var(--jp-icon-pdf);
}
.jp-PythonIcon {
  background-image: var(--jp-icon-python);
}
.jp-RKernelIcon {
  background-image: var(--jp-icon-r-kernel);
}
.jp-ReactIcon {
  background-image: var(--jp-icon-react);
}
.jp-RedoIcon {
  background-image: var(--jp-icon-redo);
}
.jp-RefreshIcon {
  background-image: var(--jp-icon-refresh);
}
.jp-RegexIcon {
  background-image: var(--jp-icon-regex);
}
.jp-RunIcon {
  background-image: var(--jp-icon-run);
}
.jp-RunningIcon {
  background-image: var(--jp-icon-running);
}
.jp-SaveIcon {
  background-image: var(--jp-icon-save);
}
.jp-SearchIcon {
  background-image: var(--jp-icon-search);
}
.jp-SettingsIcon {
  background-image: var(--jp-icon-settings);
}
.jp-SpreadsheetIcon {
  background-image: var(--jp-icon-spreadsheet);
}
.jp-StopIcon {
  background-image: var(--jp-icon-stop);
}
.jp-TabIcon {
  background-image: var(--jp-icon-tab);
}
.jp-TableRowsIcon {
  background-image: var(--jp-icon-table-rows);
}
.jp-TagIcon {
  background-image: var(--jp-icon-tag);
}
.jp-TerminalIcon {
  background-image: var(--jp-icon-terminal);
}
.jp-TextEditorIcon {
  background-image: var(--jp-icon-text-editor);
}
.jp-TocIcon {
  background-image: var(--jp-icon-toc);
}
.jp-TreeViewIcon {
  background-image: var(--jp-icon-tree-view);
}
.jp-TrustedIcon {
  background-image: var(--jp-icon-trusted);
}
.jp-UndoIcon {
  background-image: var(--jp-icon-undo);
}
.jp-VegaIcon {
  background-image: var(--jp-icon-vega);
}
.jp-YamlIcon {
  background-image: var(--jp-icon-yaml);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/**
 * (DEPRECATED) Support for consuming icons as CSS background images
 */

.jp-Icon,
.jp-MaterialIcon {
  background-position: center;
  background-repeat: no-repeat;
  background-size: 16px;
  min-width: 16px;
  min-height: 16px;
}

.jp-Icon-cover {
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}

/**
 * (DEPRECATED) Support for specific CSS icon sizes
 */

.jp-Icon-16 {
  background-size: 16px;
  min-width: 16px;
  min-height: 16px;
}

.jp-Icon-18 {
  background-size: 18px;
  min-width: 18px;
  min-height: 18px;
}

.jp-Icon-20 {
  background-size: 20px;
  min-width: 20px;
  min-height: 20px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/**
 * Support for icons as inline SVG HTMLElements
 */

/* recolor the primary elements of an icon */
.jp-icon0[fill] {
  fill: var(--jp-inverse-layout-color0);
}
.jp-icon1[fill] {
  fill: var(--jp-inverse-layout-color1);
}
.jp-icon2[fill] {
  fill: var(--jp-inverse-layout-color2);
}
.jp-icon3[fill] {
  fill: var(--jp-inverse-layout-color3);
}
.jp-icon4[fill] {
  fill: var(--jp-inverse-layout-color4);
}

.jp-icon0[stroke] {
  stroke: var(--jp-inverse-layout-color0);
}
.jp-icon1[stroke] {
  stroke: var(--jp-inverse-layout-color1);
}
.jp-icon2[stroke] {
  stroke: var(--jp-inverse-layout-color2);
}
.jp-icon3[stroke] {
  stroke: var(--jp-inverse-layout-color3);
}
.jp-icon4[stroke] {
  stroke: var(--jp-inverse-layout-color4);
}
/* recolor the accent elements of an icon */
.jp-icon-accent0[fill] {
  fill: var(--jp-layout-color0);
}
.jp-icon-accent1[fill] {
  fill: var(--jp-layout-color1);
}
.jp-icon-accent2[fill] {
  fill: var(--jp-layout-color2);
}
.jp-icon-accent3[fill] {
  fill: var(--jp-layout-color3);
}
.jp-icon-accent4[fill] {
  fill: var(--jp-layout-color4);
}

.jp-icon-accent0[stroke] {
  stroke: var(--jp-layout-color0);
}
.jp-icon-accent1[stroke] {
  stroke: var(--jp-layout-color1);
}
.jp-icon-accent2[stroke] {
  stroke: var(--jp-layout-color2);
}
.jp-icon-accent3[stroke] {
  stroke: var(--jp-layout-color3);
}
.jp-icon-accent4[stroke] {
  stroke: var(--jp-layout-color4);
}
/* set the color of an icon to transparent */
.jp-icon-none[fill] {
  fill: none;
}

.jp-icon-none[stroke] {
  stroke: none;
}
/* brand icon colors. Same for light and dark */
.jp-icon-brand0[fill] {
  fill: var(--jp-brand-color0);
}
.jp-icon-brand1[fill] {
  fill: var(--jp-brand-color1);
}
.jp-icon-brand2[fill] {
  fill: var(--jp-brand-color2);
}
.jp-icon-brand3[fill] {
  fill: var(--jp-brand-color3);
}
.jp-icon-brand4[fill] {
  fill: var(--jp-brand-color4);
}

.jp-icon-brand0[stroke] {
  stroke: var(--jp-brand-color0);
}
.jp-icon-brand1[stroke] {
  stroke: var(--jp-brand-color1);
}
.jp-icon-brand2[stroke] {
  stroke: var(--jp-brand-color2);
}
.jp-icon-brand3[stroke] {
  stroke: var(--jp-brand-color3);
}
.jp-icon-brand4[stroke] {
  stroke: var(--jp-brand-color4);
}
/* warn icon colors. Same for light and dark */
.jp-icon-warn0[fill] {
  fill: var(--jp-warn-color0);
}
.jp-icon-warn1[fill] {
  fill: var(--jp-warn-color1);
}
.jp-icon-warn2[fill] {
  fill: var(--jp-warn-color2);
}
.jp-icon-warn3[fill] {
  fill: var(--jp-warn-color3);
}

.jp-icon-warn0[stroke] {
  stroke: var(--jp-warn-color0);
}
.jp-icon-warn1[stroke] {
  stroke: var(--jp-warn-color1);
}
.jp-icon-warn2[stroke] {
  stroke: var(--jp-warn-color2);
}
.jp-icon-warn3[stroke] {
  stroke: var(--jp-warn-color3);
}
/* icon colors that contrast well with each other and most backgrounds */
.jp-icon-contrast0[fill] {
  fill: var(--jp-icon-contrast-color0);
}
.jp-icon-contrast1[fill] {
  fill: var(--jp-icon-contrast-color1);
}
.jp-icon-contrast2[fill] {
  fill: var(--jp-icon-contrast-color2);
}
.jp-icon-contrast3[fill] {
  fill: var(--jp-icon-contrast-color3);
}

.jp-icon-contrast0[stroke] {
  stroke: var(--jp-icon-contrast-color0);
}
.jp-icon-contrast1[stroke] {
  stroke: var(--jp-icon-contrast-color1);
}
.jp-icon-contrast2[stroke] {
  stroke: var(--jp-icon-contrast-color2);
}
.jp-icon-contrast3[stroke] {
  stroke: var(--jp-icon-contrast-color3);
}

/* CSS for icons in selected items in the settings editor */
#setting-editor .jp-PluginList .jp-mod-selected .jp-icon-selectable[fill] {
  fill: #fff;
}
#setting-editor
  .jp-PluginList
  .jp-mod-selected
  .jp-icon-selectable-inverse[fill] {
  fill: var(--jp-brand-color1);
}

/* CSS for icons in selected filebrowser listing items */
.jp-DirListing-item.jp-mod-selected .jp-icon-selectable[fill] {
  fill: #fff;
}
.jp-DirListing-item.jp-mod-selected .jp-icon-selectable-inverse[fill] {
  fill: var(--jp-brand-color1);
}

/* CSS for icons in selected tabs in the sidebar tab manager */
#tab-manager .lm-TabBar-tab.jp-mod-active .jp-icon-selectable[fill] {
  fill: #fff;
}

#tab-manager .lm-TabBar-tab.jp-mod-active .jp-icon-selectable-inverse[fill] {
  fill: var(--jp-brand-color1);
}
#tab-manager
  .lm-TabBar-tab.jp-mod-active
  .jp-icon-hover
  :hover
  .jp-icon-selectable[fill] {
  fill: var(--jp-brand-color1);
}

#tab-manager
  .lm-TabBar-tab.jp-mod-active
  .jp-icon-hover
  :hover
  .jp-icon-selectable-inverse[fill] {
  fill: #fff;
}

/**
 * TODO: come up with non css-hack solution for showing the busy icon on top
 *  of the close icon
 * CSS for complex behavior of close icon of tabs in the sidebar tab manager
 */
#tab-manager
  .lm-TabBar-tab.jp-mod-dirty
  > .lm-TabBar-tabCloseIcon
  > :not(:hover)
  > .jp-icon3[fill] {
  fill: none;
}
#tab-manager
  .lm-TabBar-tab.jp-mod-dirty
  > .lm-TabBar-tabCloseIcon
  > :not(:hover)
  > .jp-icon-busy[fill] {
  fill: var(--jp-inverse-layout-color3);
}

#tab-manager
  .lm-TabBar-tab.jp-mod-dirty.jp-mod-active
  > .lm-TabBar-tabCloseIcon
  > :not(:hover)
  > .jp-icon-busy[fill] {
  fill: #fff;
}

/**
* TODO: come up with non css-hack solution for showing the busy icon on top
*  of the close icon
* CSS for complex behavior of close icon of tabs in the main area tabbar
*/
.lm-DockPanel-tabBar
  .lm-TabBar-tab.lm-mod-closable.jp-mod-dirty
  > .lm-TabBar-tabCloseIcon
  > :not(:hover)
  > .jp-icon3[fill] {
  fill: none;
}
.lm-DockPanel-tabBar
  .lm-TabBar-tab.lm-mod-closable.jp-mod-dirty
  > .lm-TabBar-tabCloseIcon
  > :not(:hover)
  > .jp-icon-busy[fill] {
  fill: var(--jp-inverse-layout-color3);
}

/* CSS for icons in status bar */
#jp-main-statusbar .jp-mod-selected .jp-icon-selectable[fill] {
  fill: #fff;
}

#jp-main-statusbar .jp-mod-selected .jp-icon-selectable-inverse[fill] {
  fill: var(--jp-brand-color1);
}
/* special handling for splash icon CSS. While the theme CSS reloads during
   splash, the splash icon can loose theming. To prevent that, we set a
   default for its color variable */
:root {
  --jp-warn-color0: var(--md-orange-700);
}

/* not sure what to do with this one, used in filebrowser listing */
.jp-DragIcon {
  margin-right: 4px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/**
 * Support for alt colors for icons as inline SVG HTMLElements
 */

/* alt recolor the primary elements of an icon */
.jp-icon-alt .jp-icon0[fill] {
  fill: var(--jp-layout-color0);
}
.jp-icon-alt .jp-icon1[fill] {
  fill: var(--jp-layout-color1);
}
.jp-icon-alt .jp-icon2[fill] {
  fill: var(--jp-layout-color2);
}
.jp-icon-alt .jp-icon3[fill] {
  fill: var(--jp-layout-color3);
}
.jp-icon-alt .jp-icon4[fill] {
  fill: var(--jp-layout-color4);
}

.jp-icon-alt .jp-icon0[stroke] {
  stroke: var(--jp-layout-color0);
}
.jp-icon-alt .jp-icon1[stroke] {
  stroke: var(--jp-layout-color1);
}
.jp-icon-alt .jp-icon2[stroke] {
  stroke: var(--jp-layout-color2);
}
.jp-icon-alt .jp-icon3[stroke] {
  stroke: var(--jp-layout-color3);
}
.jp-icon-alt .jp-icon4[stroke] {
  stroke: var(--jp-layout-color4);
}

/* alt recolor the accent elements of an icon */
.jp-icon-alt .jp-icon-accent0[fill] {
  fill: var(--jp-inverse-layout-color0);
}
.jp-icon-alt .jp-icon-accent1[fill] {
  fill: var(--jp-inverse-layout-color1);
}
.jp-icon-alt .jp-icon-accent2[fill] {
  fill: var(--jp-inverse-layout-color2);
}
.jp-icon-alt .jp-icon-accent3[fill] {
  fill: var(--jp-inverse-layout-color3);
}
.jp-icon-alt .jp-icon-accent4[fill] {
  fill: var(--jp-inverse-layout-color4);
}

.jp-icon-alt .jp-icon-accent0[stroke] {
  stroke: var(--jp-inverse-layout-color0);
}
.jp-icon-alt .jp-icon-accent1[stroke] {
  stroke: var(--jp-inverse-layout-color1);
}
.jp-icon-alt .jp-icon-accent2[stroke] {
  stroke: var(--jp-inverse-layout-color2);
}
.jp-icon-alt .jp-icon-accent3[stroke] {
  stroke: var(--jp-inverse-layout-color3);
}
.jp-icon-alt .jp-icon-accent4[stroke] {
  stroke: var(--jp-inverse-layout-color4);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-icon-hoverShow:not(:hover) svg {
  display: none !important;
}

/**
 * Support for hover colors for icons as inline SVG HTMLElements
 */

/**
 * regular colors
 */

/* recolor the primary elements of an icon */
.jp-icon-hover :hover .jp-icon0-hover[fill] {
  fill: var(--jp-inverse-layout-color0);
}
.jp-icon-hover :hover .jp-icon1-hover[fill] {
  fill: var(--jp-inverse-layout-color1);
}
.jp-icon-hover :hover .jp-icon2-hover[fill] {
  fill: var(--jp-inverse-layout-color2);
}
.jp-icon-hover :hover .jp-icon3-hover[fill] {
  fill: var(--jp-inverse-layout-color3);
}
.jp-icon-hover :hover .jp-icon4-hover[fill] {
  fill: var(--jp-inverse-layout-color4);
}

.jp-icon-hover :hover .jp-icon0-hover[stroke] {
  stroke: var(--jp-inverse-layout-color0);
}
.jp-icon-hover :hover .jp-icon1-hover[stroke] {
  stroke: var(--jp-inverse-layout-color1);
}
.jp-icon-hover :hover .jp-icon2-hover[stroke] {
  stroke: var(--jp-inverse-layout-color2);
}
.jp-icon-hover :hover .jp-icon3-hover[stroke] {
  stroke: var(--jp-inverse-layout-color3);
}
.jp-icon-hover :hover .jp-icon4-hover[stroke] {
  stroke: var(--jp-inverse-layout-color4);
}

/* recolor the accent elements of an icon */
.jp-icon-hover :hover .jp-icon-accent0-hover[fill] {
  fill: var(--jp-layout-color0);
}
.jp-icon-hover :hover .jp-icon-accent1-hover[fill] {
  fill: var(--jp-layout-color1);
}
.jp-icon-hover :hover .jp-icon-accent2-hover[fill] {
  fill: var(--jp-layout-color2);
}
.jp-icon-hover :hover .jp-icon-accent3-hover[fill] {
  fill: var(--jp-layout-color3);
}
.jp-icon-hover :hover .jp-icon-accent4-hover[fill] {
  fill: var(--jp-layout-color4);
}

.jp-icon-hover :hover .jp-icon-accent0-hover[stroke] {
  stroke: var(--jp-layout-color0);
}
.jp-icon-hover :hover .jp-icon-accent1-hover[stroke] {
  stroke: var(--jp-layout-color1);
}
.jp-icon-hover :hover .jp-icon-accent2-hover[stroke] {
  stroke: var(--jp-layout-color2);
}
.jp-icon-hover :hover .jp-icon-accent3-hover[stroke] {
  stroke: var(--jp-layout-color3);
}
.jp-icon-hover :hover .jp-icon-accent4-hover[stroke] {
  stroke: var(--jp-layout-color4);
}

/* set the color of an icon to transparent */
.jp-icon-hover :hover .jp-icon-none-hover[fill] {
  fill: none;
}

.jp-icon-hover :hover .jp-icon-none-hover[stroke] {
  stroke: none;
}

/**
 * inverse colors
 */

/* inverse recolor the primary elements of an icon */
.jp-icon-hover.jp-icon-alt :hover .jp-icon0-hover[fill] {
  fill: var(--jp-layout-color0);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon1-hover[fill] {
  fill: var(--jp-layout-color1);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon2-hover[fill] {
  fill: var(--jp-layout-color2);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon3-hover[fill] {
  fill: var(--jp-layout-color3);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon4-hover[fill] {
  fill: var(--jp-layout-color4);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon0-hover[stroke] {
  stroke: var(--jp-layout-color0);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon1-hover[stroke] {
  stroke: var(--jp-layout-color1);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon2-hover[stroke] {
  stroke: var(--jp-layout-color2);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon3-hover[stroke] {
  stroke: var(--jp-layout-color3);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon4-hover[stroke] {
  stroke: var(--jp-layout-color4);
}

/* inverse recolor the accent elements of an icon */
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent0-hover[fill] {
  fill: var(--jp-inverse-layout-color0);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent1-hover[fill] {
  fill: var(--jp-inverse-layout-color1);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent2-hover[fill] {
  fill: var(--jp-inverse-layout-color2);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent3-hover[fill] {
  fill: var(--jp-inverse-layout-color3);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent4-hover[fill] {
  fill: var(--jp-inverse-layout-color4);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent0-hover[stroke] {
  stroke: var(--jp-inverse-layout-color0);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent1-hover[stroke] {
  stroke: var(--jp-inverse-layout-color1);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent2-hover[stroke] {
  stroke: var(--jp-inverse-layout-color2);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent3-hover[stroke] {
  stroke: var(--jp-inverse-layout-color3);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent4-hover[stroke] {
  stroke: var(--jp-inverse-layout-color4);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-switch {
  display: flex;
  align-items: center;
  padding-left: 4px;
  padding-right: 4px;
  font-size: var(--jp-ui-font-size1);
  background-color: transparent;
  color: var(--jp-ui-font-color1);
  border: none;
  height: 20px;
}

.jp-switch:hover {
  background-color: var(--jp-layout-color2);
}

.jp-switch-label {
  margin-right: 5px;
}

.jp-switch-track {
  cursor: pointer;
  background-color: var(--jp-border-color1);
  -webkit-transition: 0.4s;
  transition: 0.4s;
  border-radius: 34px;
  height: 16px;
  width: 35px;
  position: relative;
}

.jp-switch-track::before {
  content: '';
  position: absolute;
  height: 10px;
  width: 10px;
  margin: 3px;
  left: 0px;
  background-color: var(--jp-ui-inverse-font-color1);
  -webkit-transition: 0.4s;
  transition: 0.4s;
  border-radius: 50%;
}

.jp-switch[aria-checked='true'] .jp-switch-track {
  background-color: var(--jp-warn-color0);
}

.jp-switch[aria-checked='true'] .jp-switch-track::before {
  /* track width (35) - margins (3 + 3) - thumb width (10) */
  left: 19px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/* Sibling imports */

/* Override Blueprint's _reset.scss styles */
html {
  box-sizing: unset;
}

*,
*::before,
*::after {
  box-sizing: unset;
}

body {
  color: unset;
  font-family: var(--jp-ui-font-family);
}

p {
  margin-top: unset;
  margin-bottom: unset;
}

small {
  font-size: unset;
}

strong {
  font-weight: unset;
}

/* Override Blueprint's _typography.scss styles */
a {
  text-decoration: unset;
  color: unset;
}
a:hover {
  text-decoration: unset;
  color: unset;
}

/* Override Blueprint's _accessibility.scss styles */
:focus {
  outline: unset;
  outline-offset: unset;
  -moz-outline-radius: unset;
}

/* Styles for ui-components */
.jp-Button {
  border-radius: var(--jp-border-radius);
  padding: 0px 12px;
  font-size: var(--jp-ui-font-size1);
}

/* Use our own theme for hover styles */
button.jp-Button.bp3-button.bp3-minimal:hover {
  background-color: var(--jp-layout-color2);
}
.jp-Button.minimal {
  color: unset !important;
}

.jp-Button.jp-ToolbarButtonComponent {
  text-transform: none;
}

.jp-InputGroup input {
  box-sizing: border-box;
  border-radius: 0;
  background-color: transparent;
  color: var(--jp-ui-font-color0);
  box-shadow: inset 0 0 0 var(--jp-border-width) var(--jp-input-border-color);
}

.jp-InputGroup input:focus {
  box-shadow: inset 0 0 0 var(--jp-border-width)
      var(--jp-input-active-box-shadow-color),
    inset 0 0 0 3px var(--jp-input-active-box-shadow-color);
}

.jp-InputGroup input::placeholder,
input::placeholder {
  color: var(--jp-ui-font-color3);
}

.jp-BPIcon {
  display: inline-block;
  vertical-align: middle;
  margin: auto;
}

/* Stop blueprint futzing with our icon fills */
.bp3-icon.jp-BPIcon > svg:not([fill]) {
  fill: var(--jp-inverse-layout-color3);
}

.jp-InputGroupAction {
  padding: 6px;
}

.jp-HTMLSelect.jp-DefaultStyle select {
  background-color: initial;
  border: none;
  border-radius: 0;
  box-shadow: none;
  color: var(--jp-ui-font-color0);
  display: block;
  font-size: var(--jp-ui-font-size1);
  height: 24px;
  line-height: 14px;
  padding: 0 25px 0 10px;
  text-align: left;
  -moz-appearance: none;
  -webkit-appearance: none;
}

/* Use our own theme for hover and option styles */
.jp-HTMLSelect.jp-DefaultStyle select:hover,
.jp-HTMLSelect.jp-DefaultStyle select > option {
  background-color: var(--jp-layout-color2);
  color: var(--jp-ui-font-color0);
}
select {
  box-sizing: border-box;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-Collapse {
  display: flex;
  flex-direction: column;
  align-items: stretch;
  border-top: 1px solid var(--jp-border-color2);
  border-bottom: 1px solid var(--jp-border-color2);
}

.jp-Collapse-header {
  padding: 1px 12px;
  color: var(--jp-ui-font-color1);
  background-color: var(--jp-layout-color1);
  font-size: var(--jp-ui-font-size2);
}

.jp-Collapse-header:hover {
  background-color: var(--jp-layout-color2);
}

.jp-Collapse-contents {
  padding: 0px 12px 0px 12px;
  background-color: var(--jp-layout-color1);
  color: var(--jp-ui-font-color1);
  overflow: auto;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Variables
|----------------------------------------------------------------------------*/

:root {
  --jp-private-commandpalette-search-height: 28px;
}

/*-----------------------------------------------------------------------------
| Overall styles
|----------------------------------------------------------------------------*/

.lm-CommandPalette {
  padding-bottom: 0px;
  color: var(--jp-ui-font-color1);
  background: var(--jp-layout-color1);
  /* This is needed so that all font sizing of children done in ems is
   * relative to this base size */
  font-size: var(--jp-ui-font-size1);
}

/*-----------------------------------------------------------------------------
| Modal variant
|----------------------------------------------------------------------------*/

.jp-ModalCommandPalette {
  position: absolute;
  z-index: 10000;
  top: 38px;
  left: 30%;
  margin: 0;
  padding: 4px;
  width: 40%;
  box-shadow: var(--jp-elevation-z4);
  border-radius: 4px;
  background: var(--jp-layout-color0);
}

.jp-ModalCommandPalette .lm-CommandPalette {
  max-height: 40vh;
}

.jp-ModalCommandPalette .lm-CommandPalette .lm-close-icon::after {
  display: none;
}

.jp-ModalCommandPalette .lm-CommandPalette .lm-CommandPalette-header {
  display: none;
}

.jp-ModalCommandPalette .lm-CommandPalette .lm-CommandPalette-item {
  margin-left: 4px;
  margin-right: 4px;
}

.jp-ModalCommandPalette
  .lm-CommandPalette
  .lm-CommandPalette-item.lm-mod-disabled {
  display: none;
}

/*-----------------------------------------------------------------------------
| Search
|----------------------------------------------------------------------------*/

.lm-CommandPalette-search {
  padding: 4px;
  background-color: var(--jp-layout-color1);
  z-index: 2;
}

.lm-CommandPalette-wrapper {
  overflow: overlay;
  padding: 0px 9px;
  background-color: var(--jp-input-active-background);
  height: 30px;
  box-shadow: inset 0 0 0 var(--jp-border-width) var(--jp-input-border-color);
}

.lm-CommandPalette.lm-mod-focused .lm-CommandPalette-wrapper {
  box-shadow: inset 0 0 0 1px var(--jp-input-active-box-shadow-color),
    inset 0 0 0 3px var(--jp-input-active-box-shadow-color);
}

.jp-SearchIconGroup {
  color: white;
  background-color: var(--jp-brand-color1);
  position: absolute;
  top: 4px;
  right: 4px;
  padding: 5px 5px 1px 5px;
}

.jp-SearchIconGroup svg {
  height: 20px;
  width: 20px;
}

.jp-SearchIconGroup .jp-icon3[fill] {
  fill: var(--jp-layout-color0);
}

.lm-CommandPalette-input {
  background: transparent;
  width: calc(100% - 18px);
  float: left;
  border: none;
  outline: none;
  font-size: var(--jp-ui-font-size1);
  color: var(--jp-ui-font-color0);
  line-height: var(--jp-private-commandpalette-search-height);
}

.lm-CommandPalette-input::-webkit-input-placeholder,
.lm-CommandPalette-input::-moz-placeholder,
.lm-CommandPalette-input:-ms-input-placeholder {
  color: var(--jp-ui-font-color2);
  font-size: var(--jp-ui-font-size1);
}

/*-----------------------------------------------------------------------------
| Results
|----------------------------------------------------------------------------*/

.lm-CommandPalette-header:first-child {
  margin-top: 0px;
}

.lm-CommandPalette-header {
  border-bottom: solid var(--jp-border-width) var(--jp-border-color2);
  color: var(--jp-ui-font-color1);
  cursor: pointer;
  display: flex;
  font-size: var(--jp-ui-font-size0);
  font-weight: 600;
  letter-spacing: 1px;
  margin-top: 8px;
  padding: 8px 0 8px 12px;
  text-transform: uppercase;
}

.lm-CommandPalette-header.lm-mod-active {
  background: var(--jp-layout-color2);
}

.lm-CommandPalette-header > mark {
  background-color: transparent;
  font-weight: bold;
  color: var(--jp-ui-font-color1);
}

.lm-CommandPalette-item {
  padding: 4px 12px 4px 4px;
  color: var(--jp-ui-font-color1);
  font-size: var(--jp-ui-font-size1);
  font-weight: 400;
  display: flex;
}

.lm-CommandPalette-item.lm-mod-disabled {
  color: var(--jp-ui-font-color2);
}

.lm-CommandPalette-item.lm-mod-active {
  color: var(--jp-ui-inverse-font-color1);
  background: var(--jp-brand-color1);
}

.lm-CommandPalette-item.lm-mod-active .lm-CommandPalette-itemLabel > mark {
  color: var(--jp-ui-inverse-font-color0);
}

.lm-CommandPalette-item.lm-mod-active .jp-icon-selectable[fill] {
  fill: var(--jp-layout-color0);
}

.lm-CommandPalette-item.lm-mod-active .lm-CommandPalette-itemLabel > mark {
  color: var(--jp-ui-inverse-font-color0);
}

.lm-CommandPalette-item.lm-mod-active:hover:not(.lm-mod-disabled) {
  color: var(--jp-ui-inverse-font-color1);
  background: var(--jp-brand-color1);
}

.lm-CommandPalette-item:hover:not(.lm-mod-active):not(.lm-mod-disabled) {
  background: var(--jp-layout-color2);
}

.lm-CommandPalette-itemContent {
  overflow: hidden;
}

.lm-CommandPalette-itemLabel > mark {
  color: var(--jp-ui-font-color0);
  background-color: transparent;
  font-weight: bold;
}

.lm-CommandPalette-item.lm-mod-disabled mark {
  color: var(--jp-ui-font-color2);
}

.lm-CommandPalette-item .lm-CommandPalette-itemIcon {
  margin: 0 4px 0 0;
  position: relative;
  width: 16px;
  top: 2px;
  flex: 0 0 auto;
}

.lm-CommandPalette-item.lm-mod-disabled .lm-CommandPalette-itemIcon {
  opacity: 0.6;
}

.lm-CommandPalette-item .lm-CommandPalette-itemShortcut {
  flex: 0 0 auto;
}

.lm-CommandPalette-itemCaption {
  display: none;
}

.lm-CommandPalette-content {
  background-color: var(--jp-layout-color1);
}

.lm-CommandPalette-content:empty:after {
  content: 'No results';
  margin: auto;
  margin-top: 20px;
  width: 100px;
  display: block;
  font-size: var(--jp-ui-font-size2);
  font-family: var(--jp-ui-font-family);
  font-weight: lighter;
}

.lm-CommandPalette-emptyMessage {
  text-align: center;
  margin-top: 24px;
  line-height: 1.32;
  padding: 0px 8px;
  color: var(--jp-content-font-color3);
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2017, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-Dialog {
  position: absolute;
  z-index: 10000;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  top: 0px;
  left: 0px;
  margin: 0;
  padding: 0;
  width: 100%;
  height: 100%;
  background: var(--jp-dialog-background);
}

.jp-Dialog-content {
  display: flex;
  flex-direction: column;
  margin-left: auto;
  margin-right: auto;
  background: var(--jp-layout-color1);
  padding: 24px;
  padding-bottom: 12px;
  min-width: 300px;
  min-height: 150px;
  max-width: 1000px;
  max-height: 500px;
  box-sizing: border-box;
  box-shadow: var(--jp-elevation-z20);
  word-wrap: break-word;
  border-radius: var(--jp-border-radius);
  /* This is needed so that all font sizing of children done in ems is
   * relative to this base size */
  font-size: var(--jp-ui-font-size1);
  color: var(--jp-ui-font-color1);
  resize: both;
}

.jp-Dialog-button {
  overflow: visible;
}

button.jp-Dialog-button:focus {
  outline: 1px solid var(--jp-brand-color1);
  outline-offset: 4px;
  -moz-outline-radius: 0px;
}

button.jp-Dialog-button:focus::-moz-focus-inner {
  border: 0;
}

button.jp-Dialog-close-button {
  padding: 0;
  height: 100%;
  min-width: unset;
  min-height: unset;
}

.jp-Dialog-header {
  display: flex;
  justify-content: space-between;
  flex: 0 0 auto;
  padding-bottom: 12px;
  font-size: var(--jp-ui-font-size3);
  font-weight: 400;
  color: var(--jp-ui-font-color0);
}

.jp-Dialog-body {
  display: flex;
  flex-direction: column;
  flex: 1 1 auto;
  font-size: var(--jp-ui-font-size1);
  background: var(--jp-layout-color1);
  overflow: auto;
}

.jp-Dialog-footer {
  display: flex;
  flex-direction: row;
  justify-content: flex-end;
  flex: 0 0 auto;
  margin-left: -12px;
  margin-right: -12px;
  padding: 12px;
}

.jp-Dialog-title {
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
}

.jp-Dialog-body > .jp-select-wrapper {
  width: 100%;
}

.jp-Dialog-body > button {
  padding: 0px 16px;
}

.jp-Dialog-body > label {
  line-height: 1.4;
  color: var(--jp-ui-font-color0);
}

.jp-Dialog-button.jp-mod-styled:not(:last-child) {
  margin-right: 12px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2016, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-HoverBox {
  position: fixed;
}

.jp-HoverBox.jp-mod-outofview {
  display: none;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-IFrame {
  width: 100%;
  height: 100%;
}

.jp-IFrame > iframe {
  border: none;
}

/*
When drag events occur, `p-mod-override-cursor` is added to the body.
Because iframes steal all cursor events, the following two rules are necessary
to suppress pointer events while resize drags are occurring. There may be a
better solution to this problem.
*/
body.lm-mod-override-cursor .jp-IFrame {
  position: relative;
}

body.lm-mod-override-cursor .jp-IFrame:before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: transparent;
}

.jp-Input-Boolean-Dialog {
  flex-direction: row-reverse;
  align-items: end;
  width: 100%;
}

.jp-Input-Boolean-Dialog > label {
  flex: 1 1 auto;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2016, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-MainAreaWidget > :focus {
  outline: none;
}

/**
 * google-material-color v1.2.6
 * https://github.com/danlevan/google-material-color
 */
:root {
  --md-red-50: #ffebee;
  --md-red-100: #ffcdd2;
  --md-red-200: #ef9a9a;
  --md-red-300: #e57373;
  --md-red-400: #ef5350;
  --md-red-500: #f44336;
  --md-red-600: #e53935;
  --md-red-700: #d32f2f;
  --md-red-800: #c62828;
  --md-red-900: #b71c1c;
  --md-red-A100: #ff8a80;
  --md-red-A200: #ff5252;
  --md-red-A400: #ff1744;
  --md-red-A700: #d50000;

  --md-pink-50: #fce4ec;
  --md-pink-100: #f8bbd0;
  --md-pink-200: #f48fb1;
  --md-pink-300: #f06292;
  --md-pink-400: #ec407a;
  --md-pink-500: #e91e63;
  --md-pink-600: #d81b60;
  --md-pink-700: #c2185b;
  --md-pink-800: #ad1457;
  --md-pink-900: #880e4f;
  --md-pink-A100: #ff80ab;
  --md-pink-A200: #ff4081;
  --md-pink-A400: #f50057;
  --md-pink-A700: #c51162;

  --md-purple-50: #f3e5f5;
  --md-purple-100: #e1bee7;
  --md-purple-200: #ce93d8;
  --md-purple-300: #ba68c8;
  --md-purple-400: #ab47bc;
  --md-purple-500: #9c27b0;
  --md-purple-600: #8e24aa;
  --md-purple-700: #7b1fa2;
  --md-purple-800: #6a1b9a;
  --md-purple-900: #4a148c;
  --md-purple-A100: #ea80fc;
  --md-purple-A200: #e040fb;
  --md-purple-A400: #d500f9;
  --md-purple-A700: #aa00ff;

  --md-deep-purple-50: #ede7f6;
  --md-deep-purple-100: #d1c4e9;
  --md-deep-purple-200: #b39ddb;
  --md-deep-purple-300: #9575cd;
  --md-deep-purple-400: #7e57c2;
  --md-deep-purple-500: #673ab7;
  --md-deep-purple-600: #5e35b1;
  --md-deep-purple-700: #512da8;
  --md-deep-purple-800: #4527a0;
  --md-deep-purple-900: #311b92;
  --md-deep-purple-A100: #b388ff;
  --md-deep-purple-A200: #7c4dff;
  --md-deep-purple-A400: #651fff;
  --md-deep-purple-A700: #6200ea;

  --md-indigo-50: #e8eaf6;
  --md-indigo-100: #c5cae9;
  --md-indigo-200: #9fa8da;
  --md-indigo-300: #7986cb;
  --md-indigo-400: #5c6bc0;
  --md-indigo-500: #3f51b5;
  --md-indigo-600: #3949ab;
  --md-indigo-700: #303f9f;
  --md-indigo-800: #283593;
  --md-indigo-900: #1a237e;
  --md-indigo-A100: #8c9eff;
  --md-indigo-A200: #536dfe;
  --md-indigo-A400: #3d5afe;
  --md-indigo-A700: #304ffe;

  --md-blue-50: #e3f2fd;
  --md-blue-100: #bbdefb;
  --md-blue-200: #90caf9;
  --md-blue-300: #64b5f6;
  --md-blue-400: #42a5f5;
  --md-blue-500: #2196f3;
  --md-blue-600: #1e88e5;
  --md-blue-700: #1976d2;
  --md-blue-800: #1565c0;
  --md-blue-900: #0d47a1;
  --md-blue-A100: #82b1ff;
  --md-blue-A200: #448aff;
  --md-blue-A400: #2979ff;
  --md-blue-A700: #2962ff;

  --md-light-blue-50: #e1f5fe;
  --md-light-blue-100: #b3e5fc;
  --md-light-blue-200: #81d4fa;
  --md-light-blue-300: #4fc3f7;
  --md-light-blue-400: #29b6f6;
  --md-light-blue-500: #03a9f4;
  --md-light-blue-600: #039be5;
  --md-light-blue-700: #0288d1;
  --md-light-blue-800: #0277bd;
  --md-light-blue-900: #01579b;
  --md-light-blue-A100: #80d8ff;
  --md-light-blue-A200: #40c4ff;
  --md-light-blue-A400: #00b0ff;
  --md-light-blue-A700: #0091ea;

  --md-cyan-50: #e0f7fa;
  --md-cyan-100: #b2ebf2;
  --md-cyan-200: #80deea;
  --md-cyan-300: #4dd0e1;
  --md-cyan-400: #26c6da;
  --md-cyan-500: #00bcd4;
  --md-cyan-600: #00acc1;
  --md-cyan-700: #0097a7;
  --md-cyan-800: #00838f;
  --md-cyan-900: #006064;
  --md-cyan-A100: #84ffff;
  --md-cyan-A200: #18ffff;
  --md-cyan-A400: #00e5ff;
  --md-cyan-A700: #00b8d4;

  --md-teal-50: #e0f2f1;
  --md-teal-100: #b2dfdb;
  --md-teal-200: #80cbc4;
  --md-teal-300: #4db6ac;
  --md-teal-400: #26a69a;
  --md-teal-500: #009688;
  --md-teal-600: #00897b;
  --md-teal-700: #00796b;
  --md-teal-800: #00695c;
  --md-teal-900: #004d40;
  --md-teal-A100: #a7ffeb;
  --md-teal-A200: #64ffda;
  --md-teal-A400: #1de9b6;
  --md-teal-A700: #00bfa5;

  --md-green-50: #e8f5e9;
  --md-green-100: #c8e6c9;
  --md-green-200: #a5d6a7;
  --md-green-300: #81c784;
  --md-green-400: #66bb6a;
  --md-green-500: #4caf50;
  --md-green-600: #43a047;
  --md-green-700: #388e3c;
  --md-green-800: #2e7d32;
  --md-green-900: #1b5e20;
  --md-green-A100: #b9f6ca;
  --md-green-A200: #69f0ae;
  --md-green-A400: #00e676;
  --md-green-A700: #00c853;

  --md-light-green-50: #f1f8e9;
  --md-light-green-100: #dcedc8;
  --md-light-green-200: #c5e1a5;
  --md-light-green-300: #aed581;
  --md-light-green-400: #9ccc65;
  --md-light-green-500: #8bc34a;
  --md-light-green-600: #7cb342;
  --md-light-green-700: #689f38;
  --md-light-green-800: #558b2f;
  --md-light-green-900: #33691e;
  --md-light-green-A100: #ccff90;
  --md-light-green-A200: #b2ff59;
  --md-light-green-A400: #76ff03;
  --md-light-green-A700: #64dd17;

  --md-lime-50: #f9fbe7;
  --md-lime-100: #f0f4c3;
  --md-lime-200: #e6ee9c;
  --md-lime-300: #dce775;
  --md-lime-400: #d4e157;
  --md-lime-500: #cddc39;
  --md-lime-600: #c0ca33;
  --md-lime-700: #afb42b;
  --md-lime-800: #9e9d24;
  --md-lime-900: #827717;
  --md-lime-A100: #f4ff81;
  --md-lime-A200: #eeff41;
  --md-lime-A400: #c6ff00;
  --md-lime-A700: #aeea00;

  --md-yellow-50: #fffde7;
  --md-yellow-100: #fff9c4;
  --md-yellow-200: #fff59d;
  --md-yellow-300: #fff176;
  --md-yellow-400: #ffee58;
  --md-yellow-500: #ffeb3b;
  --md-yellow-600: #fdd835;
  --md-yellow-700: #fbc02d;
  --md-yellow-800: #f9a825;
  --md-yellow-900: #f57f17;
  --md-yellow-A100: #ffff8d;
  --md-yellow-A200: #ffff00;
  --md-yellow-A400: #ffea00;
  --md-yellow-A700: #ffd600;

  --md-amber-50: #fff8e1;
  --md-amber-100: #ffecb3;
  --md-amber-200: #ffe082;
  --md-amber-300: #ffd54f;
  --md-amber-400: #ffca28;
  --md-amber-500: #ffc107;
  --md-amber-600: #ffb300;
  --md-amber-700: #ffa000;
  --md-amber-800: #ff8f00;
  --md-amber-900: #ff6f00;
  --md-amber-A100: #ffe57f;
  --md-amber-A200: #ffd740;
  --md-amber-A400: #ffc400;
  --md-amber-A700: #ffab00;

  --md-orange-50: #fff3e0;
  --md-orange-100: #ffe0b2;
  --md-orange-200: #ffcc80;
  --md-orange-300: #ffb74d;
  --md-orange-400: #ffa726;
  --md-orange-500: #ff9800;
  --md-orange-600: #fb8c00;
  --md-orange-700: #f57c00;
  --md-orange-800: #ef6c00;
  --md-orange-900: #e65100;
  --md-orange-A100: #ffd180;
  --md-orange-A200: #ffab40;
  --md-orange-A400: #ff9100;
  --md-orange-A700: #ff6d00;

  --md-deep-orange-50: #fbe9e7;
  --md-deep-orange-100: #ffccbc;
  --md-deep-orange-200: #ffab91;
  --md-deep-orange-300: #ff8a65;
  --md-deep-orange-400: #ff7043;
  --md-deep-orange-500: #ff5722;
  --md-deep-orange-600: #f4511e;
  --md-deep-orange-700: #e64a19;
  --md-deep-orange-800: #d84315;
  --md-deep-orange-900: #bf360c;
  --md-deep-orange-A100: #ff9e80;
  --md-deep-orange-A200: #ff6e40;
  --md-deep-orange-A400: #ff3d00;
  --md-deep-orange-A700: #dd2c00;

  --md-brown-50: #efebe9;
  --md-brown-100: #d7ccc8;
  --md-brown-200: #bcaaa4;
  --md-brown-300: #a1887f;
  --md-brown-400: #8d6e63;
  --md-brown-500: #795548;
  --md-brown-600: #6d4c41;
  --md-brown-700: #5d4037;
  --md-brown-800: #4e342e;
  --md-brown-900: #3e2723;

  --md-grey-50: #fafafa;
  --md-grey-100: #f5f5f5;
  --md-grey-200: #eeeeee;
  --md-grey-300: #e0e0e0;
  --md-grey-400: #bdbdbd;
  --md-grey-500: #9e9e9e;
  --md-grey-600: #757575;
  --md-grey-700: #616161;
  --md-grey-800: #424242;
  --md-grey-900: #212121;

  --md-blue-grey-50: #eceff1;
  --md-blue-grey-100: #cfd8dc;
  --md-blue-grey-200: #b0bec5;
  --md-blue-grey-300: #90a4ae;
  --md-blue-grey-400: #78909c;
  --md-blue-grey-500: #607d8b;
  --md-blue-grey-600: #546e7a;
  --md-blue-grey-700: #455a64;
  --md-blue-grey-800: #37474f;
  --md-blue-grey-900: #263238;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2017, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-Spinner {
  position: absolute;
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 10;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  background: var(--jp-layout-color0);
  outline: none;
}

.jp-SpinnerContent {
  font-size: 10px;
  margin: 50px auto;
  text-indent: -9999em;
  width: 3em;
  height: 3em;
  border-radius: 50%;
  background: var(--jp-brand-color3);
  background: linear-gradient(
    to right,
    #f37626 10%,
    rgba(255, 255, 255, 0) 42%
  );
  position: relative;
  animation: load3 1s infinite linear, fadeIn 1s;
}

.jp-SpinnerContent:before {
  width: 50%;
  height: 50%;
  background: #f37626;
  border-radius: 100% 0 0 0;
  position: absolute;
  top: 0;
  left: 0;
  content: '';
}

.jp-SpinnerContent:after {
  background: var(--jp-layout-color0);
  width: 75%;
  height: 75%;
  border-radius: 50%;
  content: '';
  margin: auto;
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  right: 0;
}

@keyframes fadeIn {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}

@keyframes load3 {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2017, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

button.jp-mod-styled {
  font-size: var(--jp-ui-font-size1);
  color: var(--jp-ui-font-color0);
  border: none;
  box-sizing: border-box;
  text-align: center;
  line-height: 32px;
  height: 32px;
  padding: 0px 12px;
  letter-spacing: 0.8px;
  outline: none;
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
}

input.jp-mod-styled {
  background: var(--jp-input-background);
  height: 28px;
  box-sizing: border-box;
  border: var(--jp-border-width) solid var(--jp-border-color1);
  padding-left: 7px;
  padding-right: 7px;
  font-size: var(--jp-ui-font-size2);
  color: var(--jp-ui-font-color0);
  outline: none;
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
}

input[type='checkbox'].jp-mod-styled {
  appearance: checkbox;
  -webkit-appearance: checkbox;
  -moz-appearance: checkbox;
  height: auto;
}

input.jp-mod-styled:focus {
  border: var(--jp-border-width) solid var(--md-blue-500);
  box-shadow: inset 0 0 4px var(--md-blue-300);
}

.jp-FileDialog-Checkbox {
  margin-top: 35px;
  display: flex;
  flex-direction: row;
  align-items: end;
  width: 100%;
}

.jp-FileDialog-Checkbox > label {
  flex: 1 1 auto;
}

.jp-select-wrapper {
  display: flex;
  position: relative;
  flex-direction: column;
  padding: 1px;
  background-color: var(--jp-layout-color1);
  height: 28px;
  box-sizing: border-box;
  margin-bottom: 12px;
}

.jp-select-wrapper.jp-mod-focused select.jp-mod-styled {
  border: var(--jp-border-width) solid var(--jp-input-active-border-color);
  box-shadow: var(--jp-input-box-shadow);
  background-color: var(--jp-input-active-background);
}

select.jp-mod-styled:hover {
  background-color: var(--jp-layout-color1);
  cursor: pointer;
  color: var(--jp-ui-font-color0);
  background-color: var(--jp-input-hover-background);
  box-shadow: inset 0 0px 1px rgba(0, 0, 0, 0.5);
}

select.jp-mod-styled {
  flex: 1 1 auto;
  height: 32px;
  width: 100%;
  font-size: var(--jp-ui-font-size2);
  background: var(--jp-input-background);
  color: var(--jp-ui-font-color0);
  padding: 0 25px 0 8px;
  border: var(--jp-border-width) solid var(--jp-input-border-color);
  border-radius: 0px;
  outline: none;
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2016, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

:root {
  --jp-private-toolbar-height: calc(
    28px + var(--jp-border-width)
  ); /* leave 28px for content */
}

.jp-Toolbar {
  color: var(--jp-ui-font-color1);
  flex: 0 0 auto;
  display: flex;
  flex-direction: row;
  border-bottom: var(--jp-border-width) solid var(--jp-toolbar-border-color);
  box-shadow: var(--jp-toolbar-box-shadow);
  background: var(--jp-toolbar-background);
  min-height: var(--jp-toolbar-micro-height);
  padding: 2px;
  z-index: 1;
  overflow-x: auto;
}

/* Toolbar items */

.jp-Toolbar > .jp-Toolbar-item.jp-Toolbar-spacer {
  flex-grow: 1;
  flex-shrink: 1;
}

.jp-Toolbar-item.jp-Toolbar-kernelStatus {
  display: inline-block;
  width: 32px;
  background-repeat: no-repeat;
  background-position: center;
  background-size: 16px;
}

.jp-Toolbar > .jp-Toolbar-item {
  flex: 0 0 auto;
  display: flex;
  padding-left: 1px;
  padding-right: 1px;
  font-size: var(--jp-ui-font-size1);
  line-height: var(--jp-private-toolbar-height);
  height: 100%;
}

/* Toolbar buttons */

/* This is the div we use to wrap the react component into a Widget */
div.jp-ToolbarButton {
  color: transparent;
  border: none;
  box-sizing: border-box;
  outline: none;
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
  padding: 0px;
  margin: 0px;
}

button.jp-ToolbarButtonComponent {
  background: var(--jp-layout-color1);
  border: none;
  box-sizing: border-box;
  outline: none;
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
  padding: 0px 6px;
  margin: 0px;
  height: 24px;
  border-radius: var(--jp-border-radius);
  display: flex;
  align-items: center;
  text-align: center;
  font-size: 14px;
  min-width: unset;
  min-height: unset;
}

button.jp-ToolbarButtonComponent:disabled {
  opacity: 0.4;
}

button.jp-ToolbarButtonComponent span {
  padding: 0px;
  flex: 0 0 auto;
}

button.jp-ToolbarButtonComponent .jp-ToolbarButtonComponent-label {
  font-size: var(--jp-ui-font-size1);
  line-height: 100%;
  padding-left: 2px;
  color: var(--jp-ui-font-color1);
}

#jp-main-dock-panel[data-mode='single-document']
  .jp-MainAreaWidget
  > .jp-Toolbar.jp-Toolbar-micro {
  padding: 0;
  min-height: 0;
}

#jp-main-dock-panel[data-mode='single-document']
  .jp-MainAreaWidget
  > .jp-Toolbar {
  border: none;
  box-shadow: none;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2017, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ body.p-mod-override-cursor *, /* </DEPRECATED> */
body.lm-mod-override-cursor * {
  cursor: inherit !important;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2016, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-JSONEditor {
  display: flex;
  flex-direction: column;
  width: 100%;
}

.jp-JSONEditor-host {
  flex: 1 1 auto;
  border: var(--jp-border-width) solid var(--jp-input-border-color);
  border-radius: 0px;
  background: var(--jp-layout-color0);
  min-height: 50px;
  padding: 1px;
}

.jp-JSONEditor.jp-mod-error .jp-JSONEditor-host {
  border-color: red;
  outline-color: red;
}

.jp-JSONEditor-header {
  display: flex;
  flex: 1 0 auto;
  padding: 0 0 0 12px;
}

.jp-JSONEditor-header label {
  flex: 0 0 auto;
}

.jp-JSONEditor-commitButton {
  height: 16px;
  width: 16px;
  background-size: 18px;
  background-repeat: no-repeat;
  background-position: center;
}

.jp-JSONEditor-host.jp-mod-focused {
  background-color: var(--jp-input-active-background);
  border: 1px solid var(--jp-input-active-border-color);
  box-shadow: var(--jp-input-box-shadow);
}

.jp-Editor.jp-mod-dropTarget {
  border: var(--jp-border-width) solid var(--jp-input-active-border-color);
  box-shadow: var(--jp-input-box-shadow);
}

/* BASICS */

.CodeMirror {
  /* Set height, width, borders, and global font properties here */
  font-family: monospace;
  height: 300px;
  color: black;
  direction: ltr;
}

/* PADDING */

.CodeMirror-lines {
  padding: 4px 0; /* Vertical padding around content */
}
.CodeMirror pre.CodeMirror-line,
.CodeMirror pre.CodeMirror-line-like {
  padding: 0 4px; /* Horizontal padding of content */
}

.CodeMirror-scrollbar-filler, .CodeMirror-gutter-filler {
  background-color: white; /* The little square between H and V scrollbars */
}

/* GUTTER */

.CodeMirror-gutters {
  border-right: 1px solid #ddd;
  background-color: #f7f7f7;
  white-space: nowrap;
}
.CodeMirror-linenumbers {}
.CodeMirror-linenumber {
  padding: 0 3px 0 5px;
  min-width: 20px;
  text-align: right;
  color: #999;
  white-space: nowrap;
}

.CodeMirror-guttermarker { color: black; }
.CodeMirror-guttermarker-subtle { color: #999; }

/* CURSOR */

.CodeMirror-cursor {
  border-left: 1px solid black;
  border-right: none;
  width: 0;
}
/* Shown when moving in bi-directional text */
.CodeMirror div.CodeMirror-secondarycursor {
  border-left: 1px solid silver;
}
.cm-fat-cursor .CodeMirror-cursor {
  width: auto;
  border: 0 !important;
  background: #7e7;
}
.cm-fat-cursor div.CodeMirror-cursors {
  z-index: 1;
}
.cm-fat-cursor-mark {
  background-color: rgba(20, 255, 20, 0.5);
  -webkit-animation: blink 1.06s steps(1) infinite;
  -moz-animation: blink 1.06s steps(1) infinite;
  animation: blink 1.06s steps(1) infinite;
}
.cm-animate-fat-cursor {
  width: auto;
  border: 0;
  -webkit-animation: blink 1.06s steps(1) infinite;
  -moz-animation: blink 1.06s steps(1) infinite;
  animation: blink 1.06s steps(1) infinite;
  background-color: #7e7;
}
@-moz-keyframes blink {
  0% {}
  50% { background-color: transparent; }
  100% {}
}
@-webkit-keyframes blink {
  0% {}
  50% { background-color: transparent; }
  100% {}
}
@keyframes blink {
  0% {}
  50% { background-color: transparent; }
  100% {}
}

/* Can style cursor different in overwrite (non-insert) mode */
.CodeMirror-overwrite .CodeMirror-cursor {}

.cm-tab { display: inline-block; text-decoration: inherit; }

.CodeMirror-rulers {
  position: absolute;
  left: 0; right: 0; top: -50px; bottom: 0;
  overflow: hidden;
}
.CodeMirror-ruler {
  border-left: 1px solid #ccc;
  top: 0; bottom: 0;
  position: absolute;
}

/* DEFAULT THEME */

.cm-s-default .cm-header {color: blue;}
.cm-s-default .cm-quote {color: #090;}
.cm-negative {color: #d44;}
.cm-positive {color: #292;}
.cm-header, .cm-strong {font-weight: bold;}
.cm-em {font-style: italic;}
.cm-link {text-decoration: underline;}
.cm-strikethrough {text-decoration: line-through;}

.cm-s-default .cm-keyword {color: #708;}
.cm-s-default .cm-atom {color: #219;}
.cm-s-default .cm-number {color: #164;}
.cm-s-default .cm-def {color: #00f;}
.cm-s-default .cm-variable,
.cm-s-default .cm-punctuation,
.cm-s-default .cm-property,
.cm-s-default .cm-operator {}
.cm-s-default .cm-variable-2 {color: #05a;}
.cm-s-default .cm-variable-3, .cm-s-default .cm-type {color: #085;}
.cm-s-default .cm-comment {color: #a50;}
.cm-s-default .cm-string {color: #a11;}
.cm-s-default .cm-string-2 {color: #f50;}
.cm-s-default .cm-meta {color: #555;}
.cm-s-default .cm-qualifier {color: #555;}
.cm-s-default .cm-builtin {color: #30a;}
.cm-s-default .cm-bracket {color: #997;}
.cm-s-default .cm-tag {color: #170;}
.cm-s-default .cm-attribute {color: #00c;}
.cm-s-default .cm-hr {color: #999;}
.cm-s-default .cm-link {color: #00c;}

.cm-s-default .cm-error {color: #f00;}
.cm-invalidchar {color: #f00;}

.CodeMirror-composing { border-bottom: 2px solid; }

/* Default styles for common addons */

div.CodeMirror span.CodeMirror-matchingbracket {color: #0b0;}
div.CodeMirror span.CodeMirror-nonmatchingbracket {color: #a22;}
.CodeMirror-matchingtag { background: rgba(255, 150, 0, .3); }
.CodeMirror-activeline-background {background: #e8f2ff;}

/* STOP */

/* The rest of this file contains styles related to the mechanics of
   the editor. You probably shouldn't touch them. */

.CodeMirror {
  position: relative;
  overflow: hidden;
  background: white;
}

.CodeMirror-scroll {
  overflow: scroll !important; /* Things will break if this is overridden */
  /* 50px is the magic margin used to hide the element's real scrollbars */
  /* See overflow: hidden in .CodeMirror */
  margin-bottom: -50px; margin-right: -50px;
  padding-bottom: 50px;
  height: 100%;
  outline: none; /* Prevent dragging from highlighting the element */
  position: relative;
}
.CodeMirror-sizer {
  position: relative;
  border-right: 50px solid transparent;
}

/* The fake, visible scrollbars. Used to force redraw during scrolling
   before actual scrolling happens, thus preventing shaking and
   flickering artifacts. */
.CodeMirror-vscrollbar, .CodeMirror-hscrollbar, .CodeMirror-scrollbar-filler, .CodeMirror-gutter-filler {
  position: absolute;
  z-index: 6;
  display: none;
  outline: none;
}
.CodeMirror-vscrollbar {
  right: 0; top: 0;
  overflow-x: hidden;
  overflow-y: scroll;
}
.CodeMirror-hscrollbar {
  bottom: 0; left: 0;
  overflow-y: hidden;
  overflow-x: scroll;
}
.CodeMirror-scrollbar-filler {
  right: 0; bottom: 0;
}
.CodeMirror-gutter-filler {
  left: 0; bottom: 0;
}

.CodeMirror-gutters {
  position: absolute; left: 0; top: 0;
  min-height: 100%;
  z-index: 3;
}
.CodeMirror-gutter {
  white-space: normal;
  height: 100%;
  display: inline-block;
  vertical-align: top;
  margin-bottom: -50px;
}
.CodeMirror-gutter-wrapper {
  position: absolute;
  z-index: 4;
  background: none !important;
  border: none !important;
}
.CodeMirror-gutter-background {
  position: absolute;
  top: 0; bottom: 0;
  z-index: 4;
}
.CodeMirror-gutter-elt {
  position: absolute;
  cursor: default;
  z-index: 4;
}
.CodeMirror-gutter-wrapper ::selection { background-color: transparent }
.CodeMirror-gutter-wrapper ::-moz-selection { background-color: transparent }

.CodeMirror-lines {
  cursor: text;
  min-height: 1px; /* prevents collapsing before first draw */
}
.CodeMirror pre.CodeMirror-line,
.CodeMirror pre.CodeMirror-line-like {
  /* Reset some styles that the rest of the page might have set */
  -moz-border-radius: 0; -webkit-border-radius: 0; border-radius: 0;
  border-width: 0;
  background: transparent;
  font-family: inherit;
  font-size: inherit;
  margin: 0;
  white-space: pre;
  word-wrap: normal;
  line-height: inherit;
  color: inherit;
  z-index: 2;
  position: relative;
  overflow: visible;
  -webkit-tap-highlight-color: transparent;
  -webkit-font-variant-ligatures: contextual;
  font-variant-ligatures: contextual;
}
.CodeMirror-wrap pre.CodeMirror-line,
.CodeMirror-wrap pre.CodeMirror-line-like {
  word-wrap: break-word;
  white-space: pre-wrap;
  word-break: normal;
}

.CodeMirror-linebackground {
  position: absolute;
  left: 0; right: 0; top: 0; bottom: 0;
  z-index: 0;
}

.CodeMirror-linewidget {
  position: relative;
  z-index: 2;
  padding: 0.1px; /* Force widget margins to stay inside of the container */
}

.CodeMirror-widget {}

.CodeMirror-rtl pre { direction: rtl; }

.CodeMirror-code {
  outline: none;
}

/* Force content-box sizing for the elements where we expect it */
.CodeMirror-scroll,
.CodeMirror-sizer,
.CodeMirror-gutter,
.CodeMirror-gutters,
.CodeMirror-linenumber {
  -moz-box-sizing: content-box;
  box-sizing: content-box;
}

.CodeMirror-measure {
  position: absolute;
  width: 100%;
  height: 0;
  overflow: hidden;
  visibility: hidden;
}

.CodeMirror-cursor {
  position: absolute;
  pointer-events: none;
}
.CodeMirror-measure pre { position: static; }

div.CodeMirror-cursors {
  visibility: hidden;
  position: relative;
  z-index: 3;
}
div.CodeMirror-dragcursors {
  visibility: visible;
}

.CodeMirror-focused div.CodeMirror-cursors {
  visibility: visible;
}

.CodeMirror-selected { background: #d9d9d9; }
.CodeMirror-focused .CodeMirror-selected { background: #d7d4f0; }
.CodeMirror-crosshair { cursor: crosshair; }
.CodeMirror-line::selection, .CodeMirror-line > span::selection, .CodeMirror-line > span > span::selection { background: #d7d4f0; }
.CodeMirror-line::-moz-selection, .CodeMirror-line > span::-moz-selection, .CodeMirror-line > span > span::-moz-selection { background: #d7d4f0; }

.cm-searching {
  background-color: #ffa;
  background-color: rgba(255, 255, 0, .4);
}

/* Used to force a border model for a node */
.cm-force-border { padding-right: .1px; }

@media print {
  /* Hide the cursor when printing */
  .CodeMirror div.CodeMirror-cursors {
    visibility: hidden;
  }
}

/* See issue #2901 */
.cm-tab-wrap-hack:after { content: ''; }

/* Help users use markselection to safely style text background */
span.CodeMirror-selectedtext { background: none; }

.CodeMirror-dialog {
  position: absolute;
  left: 0; right: 0;
  background: inherit;
  z-index: 15;
  padding: .1em .8em;
  overflow: hidden;
  color: inherit;
}

.CodeMirror-dialog-top {
  border-bottom: 1px solid #eee;
  top: 0;
}

.CodeMirror-dialog-bottom {
  border-top: 1px solid #eee;
  bottom: 0;
}

.CodeMirror-dialog input {
  border: none;
  outline: none;
  background: transparent;
  width: 20em;
  color: inherit;
  font-family: monospace;
}

.CodeMirror-dialog button {
  font-size: 70%;
}

.CodeMirror-foldmarker {
  color: blue;
  text-shadow: #b9f 1px 1px 2px, #b9f -1px -1px 2px, #b9f 1px -1px 2px, #b9f -1px 1px 2px;
  font-family: arial;
  line-height: .3;
  cursor: pointer;
}
.CodeMirror-foldgutter {
  width: .7em;
}
.CodeMirror-foldgutter-open,
.CodeMirror-foldgutter-folded {
  cursor: pointer;
}
.CodeMirror-foldgutter-open:after {
  content: "\25BE";
}
.CodeMirror-foldgutter-folded:after {
  content: "\25B8";
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.CodeMirror {
  line-height: var(--jp-code-line-height);
  font-size: var(--jp-code-font-size);
  font-family: var(--jp-code-font-family);
  border: 0;
  border-radius: 0;
  height: auto;
  /* Changed to auto to autogrow */
}

.CodeMirror pre {
  padding: 0 var(--jp-code-padding);
}

.jp-CodeMirrorEditor[data-type='inline'] .CodeMirror-dialog {
  background-color: var(--jp-layout-color0);
  color: var(--jp-content-font-color1);
}

/* This causes https://github.com/jupyter/jupyterlab/issues/522 */
/* May not cause it not because we changed it! */
.CodeMirror-lines {
  padding: var(--jp-code-padding) 0;
}

.CodeMirror-linenumber {
  padding: 0 8px;
}

.jp-CodeMirrorEditor {
  cursor: text;
}

.jp-CodeMirrorEditor[data-type='inline'] .CodeMirror-cursor {
  border-left: var(--jp-code-cursor-width0) solid var(--jp-editor-cursor-color);
}

/* When zoomed out 67% and 33% on a screen of 1440 width x 900 height */
@media screen and (min-width: 2138px) and (max-width: 4319px) {
  .jp-CodeMirrorEditor[data-type='inline'] .CodeMirror-cursor {
    border-left: var(--jp-code-cursor-width1) solid
      var(--jp-editor-cursor-color);
  }
}

/* When zoomed out less than 33% */
@media screen and (min-width: 4320px) {
  .jp-CodeMirrorEditor[data-type='inline'] .CodeMirror-cursor {
    border-left: var(--jp-code-cursor-width2) solid
      var(--jp-editor-cursor-color);
  }
}

.CodeMirror.jp-mod-readOnly .CodeMirror-cursor {
  display: none;
}

.CodeMirror-gutters {
  border-right: 1px solid var(--jp-border-color2);
  background-color: var(--jp-layout-color0);
}

.jp-CollaboratorCursor {
  border-left: 5px solid transparent;
  border-right: 5px solid transparent;
  border-top: none;
  border-bottom: 3px solid;
  background-clip: content-box;
  margin-left: -5px;
  margin-right: -5px;
}

.CodeMirror-selectedtext.cm-searching {
  background-color: var(--jp-search-selected-match-background-color) !important;
  color: var(--jp-search-selected-match-color) !important;
}

.cm-searching {
  background-color: var(
    --jp-search-unselected-match-background-color
  ) !important;
  color: var(--jp-search-unselected-match-color) !important;
}

.CodeMirror-focused .CodeMirror-selected {
  background-color: var(--jp-editor-selected-focused-background);
}

.CodeMirror-selected {
  background-color: var(--jp-editor-selected-background);
}

.jp-CollaboratorCursor-hover {
  position: absolute;
  z-index: 1;
  transform: translateX(-50%);
  color: white;
  border-radius: 3px;
  padding-left: 4px;
  padding-right: 4px;
  padding-top: 1px;
  padding-bottom: 1px;
  text-align: center;
  font-size: var(--jp-ui-font-size1);
  white-space: nowrap;
}

.jp-CodeMirror-ruler {
  border-left: 1px dashed var(--jp-border-color2);
}

/**
 * Here is our jupyter theme for CodeMirror syntax highlighting
 * This is used in our marked.js syntax highlighting and CodeMirror itself
 * The string "jupyter" is set in ../codemirror/widget.DEFAULT_CODEMIRROR_THEME
 * This came from the classic notebook, which came form highlight.js/GitHub
 */

/**
 * CodeMirror themes are handling the background/color in this way. This works
 * fine for CodeMirror editors outside the notebook, but the notebook styles
 * these things differently.
 */
.CodeMirror.cm-s-jupyter {
  background: var(--jp-layout-color0);
  color: var(--jp-content-font-color1);
}

/* In the notebook, we want this styling to be handled by its container */
.jp-CodeConsole .CodeMirror.cm-s-jupyter,
.jp-Notebook .CodeMirror.cm-s-jupyter {
  background: transparent;
}

.cm-s-jupyter .CodeMirror-cursor {
  border-left: var(--jp-code-cursor-width0) solid var(--jp-editor-cursor-color);
}
.cm-s-jupyter span.cm-keyword {
  color: var(--jp-mirror-editor-keyword-color);
  font-weight: bold;
}
.cm-s-jupyter span.cm-atom {
  color: var(--jp-mirror-editor-atom-color);
}
.cm-s-jupyter span.cm-number {
  color: var(--jp-mirror-editor-number-color);
}
.cm-s-jupyter span.cm-def {
  color: var(--jp-mirror-editor-def-color);
}
.cm-s-jupyter span.cm-variable {
  color: var(--jp-mirror-editor-variable-color);
}
.cm-s-jupyter span.cm-variable-2 {
  color: var(--jp-mirror-editor-variable-2-color);
}
.cm-s-jupyter span.cm-variable-3 {
  color: var(--jp-mirror-editor-variable-3-color);
}
.cm-s-jupyter span.cm-punctuation {
  color: var(--jp-mirror-editor-punctuation-color);
}
.cm-s-jupyter span.cm-property {
  color: var(--jp-mirror-editor-property-color);
}
.cm-s-jupyter span.cm-operator {
  color: var(--jp-mirror-editor-operator-color);
  font-weight: bold;
}
.cm-s-jupyter span.cm-comment {
  color: var(--jp-mirror-editor-comment-color);
  font-style: italic;
}
.cm-s-jupyter span.cm-string {
  color: var(--jp-mirror-editor-string-color);
}
.cm-s-jupyter span.cm-string-2 {
  color: var(--jp-mirror-editor-string-2-color);
}
.cm-s-jupyter span.cm-meta {
  color: var(--jp-mirror-editor-meta-color);
}
.cm-s-jupyter span.cm-qualifier {
  color: var(--jp-mirror-editor-qualifier-color);
}
.cm-s-jupyter span.cm-builtin {
  color: var(--jp-mirror-editor-builtin-color);
}
.cm-s-jupyter span.cm-bracket {
  color: var(--jp-mirror-editor-bracket-color);
}
.cm-s-jupyter span.cm-tag {
  color: var(--jp-mirror-editor-tag-color);
}
.cm-s-jupyter span.cm-attribute {
  color: var(--jp-mirror-editor-attribute-color);
}
.cm-s-jupyter span.cm-header {
  color: var(--jp-mirror-editor-header-color);
}
.cm-s-jupyter span.cm-quote {
  color: var(--jp-mirror-editor-quote-color);
}
.cm-s-jupyter span.cm-link {
  color: var(--jp-mirror-editor-link-color);
}
.cm-s-jupyter span.cm-error {
  color: var(--jp-mirror-editor-error-color);
}
.cm-s-jupyter span.cm-hr {
  color: #999;
}

.cm-s-jupyter span.cm-tab {
  background: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADAAAAAMCAYAAAAkuj5RAAAAAXNSR0IArs4c6QAAAGFJREFUSMft1LsRQFAQheHPowAKoACx3IgEKtaEHujDjORSgWTH/ZOdnZOcM/sgk/kFFWY0qV8foQwS4MKBCS3qR6ixBJvElOobYAtivseIE120FaowJPN75GMu8j/LfMwNjh4HUpwg4LUAAAAASUVORK5CYII=);
  background-position: right;
  background-repeat: no-repeat;
}

.cm-s-jupyter .CodeMirror-activeline-background,
.cm-s-jupyter .CodeMirror-gutter {
  background-color: var(--jp-layout-color2);
}

/* Styles for shared cursors (remote cursor locations and selected ranges) */
.jp-CodeMirrorEditor .remote-caret {
  position: relative;
  border-left: 2px solid black;
  margin-left: -1px;
  margin-right: -1px;
  box-sizing: border-box;
}

.jp-CodeMirrorEditor .remote-caret > div {
  white-space: nowrap;
  position: absolute;
  top: -1.15em;
  padding-bottom: 0.05em;
  left: -2px;
  font-size: 0.95em;
  background-color: rgb(250, 129, 0);
  font-family: var(--jp-ui-font-family);
  font-weight: bold;
  line-height: normal;
  user-select: none;
  color: white;
  padding-left: 2px;
  padding-right: 2px;
  z-index: 3;
  transition: opacity 0.3s ease-in-out;
}

.jp-CodeMirrorEditor .remote-caret.hide-name > div {
  transition-delay: 0.7s;
  opacity: 0;
}

.jp-CodeMirrorEditor .remote-caret:hover > div {
  opacity: 1;
  transition-delay: 0s;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| RenderedText
|----------------------------------------------------------------------------*/

:root {
  /* This is the padding value to fill the gaps between lines containing spans with background color. */
  --jp-private-code-span-padding: calc(
    (var(--jp-code-line-height) - 1) * var(--jp-code-font-size) / 2
  );
}

.jp-RenderedText {
  text-align: left;
  padding-left: var(--jp-code-padding);
  line-height: var(--jp-code-line-height);
  font-family: var(--jp-code-font-family);
}

.jp-RenderedText pre,
.jp-RenderedJavaScript pre,
.jp-RenderedHTMLCommon pre {
  color: var(--jp-content-font-color1);
  font-size: var(--jp-code-font-size);
  border: none;
  margin: 0px;
  padding: 0px;
}

.jp-RenderedText pre a:link {
  text-decoration: none;
  color: var(--jp-content-link-color);
}
.jp-RenderedText pre a:hover {
  text-decoration: underline;
  color: var(--jp-content-link-color);
}
.jp-RenderedText pre a:visited {
  text-decoration: none;
  color: var(--jp-content-link-color);
}

/* console foregrounds and backgrounds */
.jp-RenderedText pre .ansi-black-fg {
  color: #3e424d;
}
.jp-RenderedText pre .ansi-red-fg {
  color: #e75c58;
}
.jp-RenderedText pre .ansi-green-fg {
  color: #00a250;
}
.jp-RenderedText pre .ansi-yellow-fg {
  color: #ddb62b;
}
.jp-RenderedText pre .ansi-blue-fg {
  color: #208ffb;
}
.jp-RenderedText pre .ansi-magenta-fg {
  color: #d160c4;
}
.jp-RenderedText pre .ansi-cyan-fg {
  color: #60c6c8;
}
.jp-RenderedText pre .ansi-white-fg {
  color: #c5c1b4;
}

.jp-RenderedText pre .ansi-black-bg {
  background-color: #3e424d;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-red-bg {
  background-color: #e75c58;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-green-bg {
  background-color: #00a250;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-yellow-bg {
  background-color: #ddb62b;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-blue-bg {
  background-color: #208ffb;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-magenta-bg {
  background-color: #d160c4;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-cyan-bg {
  background-color: #60c6c8;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-white-bg {
  background-color: #c5c1b4;
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-black-intense-fg {
  color: #282c36;
}
.jp-RenderedText pre .ansi-red-intense-fg {
  color: #b22b31;
}
.jp-RenderedText pre .ansi-green-intense-fg {
  color: #007427;
}
.jp-RenderedText pre .ansi-yellow-intense-fg {
  color: #b27d12;
}
.jp-RenderedText pre .ansi-blue-intense-fg {
  color: #0065ca;
}
.jp-RenderedText pre .ansi-magenta-intense-fg {
  color: #a03196;
}
.jp-RenderedText pre .ansi-cyan-intense-fg {
  color: #258f8f;
}
.jp-RenderedText pre .ansi-white-intense-fg {
  color: #a1a6b2;
}

.jp-RenderedText pre .ansi-black-intense-bg {
  background-color: #282c36;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-red-intense-bg {
  background-color: #b22b31;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-green-intense-bg {
  background-color: #007427;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-yellow-intense-bg {
  background-color: #b27d12;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-blue-intense-bg {
  background-color: #0065ca;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-magenta-intense-bg {
  background-color: #a03196;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-cyan-intense-bg {
  background-color: #258f8f;
  padding: var(--jp-private-code-span-padding) 0;
}
.jp-RenderedText pre .ansi-white-intense-bg {
  background-color: #a1a6b2;
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-default-inverse-fg {
  color: var(--jp-ui-inverse-font-color0);
}
.jp-RenderedText pre .ansi-default-inverse-bg {
  background-color: var(--jp-inverse-layout-color0);
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-bold {
  font-weight: bold;
}
.jp-RenderedText pre .ansi-underline {
  text-decoration: underline;
}

.jp-RenderedText[data-mime-type='application/vnd.jupyter.stderr'] {
  background: var(--jp-rendermime-error-background);
  padding-top: var(--jp-code-padding);
}

/*-----------------------------------------------------------------------------
| RenderedLatex
|----------------------------------------------------------------------------*/

.jp-RenderedLatex {
  color: var(--jp-content-font-color1);
  font-size: var(--jp-content-font-size1);
  line-height: var(--jp-content-line-height);
}

/* Left-justify outputs.*/
.jp-OutputArea-output.jp-RenderedLatex {
  padding: var(--jp-code-padding);
  text-align: left;
}

/*-----------------------------------------------------------------------------
| RenderedHTML
|----------------------------------------------------------------------------*/

.jp-RenderedHTMLCommon {
  color: var(--jp-content-font-color1);
  font-family: var(--jp-content-font-family);
  font-size: var(--jp-content-font-size1);
  line-height: var(--jp-content-line-height);
  /* Give a bit more R padding on Markdown text to keep line lengths reasonable */
  padding-right: 20px;
}

.jp-RenderedHTMLCommon em {
  font-style: italic;
}

.jp-RenderedHTMLCommon strong {
  font-weight: bold;
}

.jp-RenderedHTMLCommon u {
  text-decoration: underline;
}

.jp-RenderedHTMLCommon a:link {
  text-decoration: none;
  color: var(--jp-content-link-color);
}

.jp-RenderedHTMLCommon a:hover {
  text-decoration: underline;
  color: var(--jp-content-link-color);
}

.jp-RenderedHTMLCommon a:visited {
  text-decoration: none;
  color: var(--jp-content-link-color);
}

/* Headings */

.jp-RenderedHTMLCommon h1,
.jp-RenderedHTMLCommon h2,
.jp-RenderedHTMLCommon h3,
.jp-RenderedHTMLCommon h4,
.jp-RenderedHTMLCommon h5,
.jp-RenderedHTMLCommon h6 {
  line-height: var(--jp-content-heading-line-height);
  font-weight: var(--jp-content-heading-font-weight);
  font-style: normal;
  margin: var(--jp-content-heading-margin-top) 0
    var(--jp-content-heading-margin-bottom) 0;
}

.jp-RenderedHTMLCommon h1:first-child,
.jp-RenderedHTMLCommon h2:first-child,
.jp-RenderedHTMLCommon h3:first-child,
.jp-RenderedHTMLCommon h4:first-child,
.jp-RenderedHTMLCommon h5:first-child,
.jp-RenderedHTMLCommon h6:first-child {
  margin-top: calc(0.5 * var(--jp-content-heading-margin-top));
}

.jp-RenderedHTMLCommon h1:last-child,
.jp-RenderedHTMLCommon h2:last-child,
.jp-RenderedHTMLCommon h3:last-child,
.jp-RenderedHTMLCommon h4:last-child,
.jp-RenderedHTMLCommon h5:last-child,
.jp-RenderedHTMLCommon h6:last-child {
  margin-bottom: calc(0.5 * var(--jp-content-heading-margin-bottom));
}

.jp-RenderedHTMLCommon h1 {
  font-size: var(--jp-content-font-size5);
}

.jp-RenderedHTMLCommon h2 {
  font-size: var(--jp-content-font-size4);
}

.jp-RenderedHTMLCommon h3 {
  font-size: var(--jp-content-font-size3);
}

.jp-RenderedHTMLCommon h4 {
  font-size: var(--jp-content-font-size2);
}

.jp-RenderedHTMLCommon h5 {
  font-size: var(--jp-content-font-size1);
}

.jp-RenderedHTMLCommon h6 {
  font-size: var(--jp-content-font-size0);
}

/* Lists */

.jp-RenderedHTMLCommon ul:not(.list-inline),
.jp-RenderedHTMLCommon ol:not(.list-inline) {
  padding-left: 2em;
}

.jp-RenderedHTMLCommon ul {
  list-style: disc;
}

.jp-RenderedHTMLCommon ul ul {
  list-style: square;
}

.jp-RenderedHTMLCommon ul ul ul {
  list-style: circle;
}

.jp-RenderedHTMLCommon ol {
  list-style: decimal;
}

.jp-RenderedHTMLCommon ol ol {
  list-style: upper-alpha;
}

.jp-RenderedHTMLCommon ol ol ol {
  list-style: lower-alpha;
}

.jp-RenderedHTMLCommon ol ol ol ol {
  list-style: lower-roman;
}

.jp-RenderedHTMLCommon ol ol ol ol ol {
  list-style: decimal;
}

.jp-RenderedHTMLCommon ol,
.jp-RenderedHTMLCommon ul {
  margin-bottom: 1em;
}

.jp-RenderedHTMLCommon ul ul,
.jp-RenderedHTMLCommon ul ol,
.jp-RenderedHTMLCommon ol ul,
.jp-RenderedHTMLCommon ol ol {
  margin-bottom: 0em;
}

.jp-RenderedHTMLCommon hr {
  color: var(--jp-border-color2);
  background-color: var(--jp-border-color1);
  margin-top: 1em;
  margin-bottom: 1em;
}

.jp-RenderedHTMLCommon > pre {
  margin: 1.5em 2em;
}

.jp-RenderedHTMLCommon pre,
.jp-RenderedHTMLCommon code {
  border: 0;
  background-color: var(--jp-layout-color0);
  color: var(--jp-content-font-color1);
  font-family: var(--jp-code-font-family);
  font-size: inherit;
  line-height: var(--jp-code-line-height);
  padding: 0;
  white-space: pre-wrap;
}

.jp-RenderedHTMLCommon :not(pre) > code {
  background-color: var(--jp-layout-color2);
  padding: 1px 5px;
}

/* Tables */

.jp-RenderedHTMLCommon table {
  border-collapse: collapse;
  border-spacing: 0;
  border: none;
  color: var(--jp-ui-font-color1);
  font-size: 12px;
  table-layout: fixed;
  margin-left: auto;
  margin-right: auto;
}

.jp-RenderedHTMLCommon thead {
  border-bottom: var(--jp-border-width) solid var(--jp-border-color1);
  vertical-align: bottom;
}

.jp-RenderedHTMLCommon td,
.jp-RenderedHTMLCommon th,
.jp-RenderedHTMLCommon tr {
  vertical-align: middle;
  padding: 0.5em 0.5em;
  line-height: normal;
  white-space: normal;
  max-width: none;
  border: none;
}

.jp-RenderedMarkdown.jp-RenderedHTMLCommon td,
.jp-RenderedMarkdown.jp-RenderedHTMLCommon th {
  max-width: none;
}

:not(.jp-RenderedMarkdown).jp-RenderedHTMLCommon td,
:not(.jp-RenderedMarkdown).jp-RenderedHTMLCommon th,
:not(.jp-RenderedMarkdown).jp-RenderedHTMLCommon tr {
  text-align: right;
}

.jp-RenderedHTMLCommon th {
  font-weight: bold;
}

.jp-RenderedHTMLCommon tbody tr:nth-child(odd) {
  background: var(--jp-layout-color0);
}

.jp-RenderedHTMLCommon tbody tr:nth-child(even) {
  background: var(--jp-rendermime-table-row-background);
}

.jp-RenderedHTMLCommon tbody tr:hover {
  background: var(--jp-rendermime-table-row-hover-background);
}

.jp-RenderedHTMLCommon table {
  margin-bottom: 1em;
}

.jp-RenderedHTMLCommon p {
  text-align: left;
  margin: 0px;
}

.jp-RenderedHTMLCommon p {
  margin-bottom: 1em;
}

.jp-RenderedHTMLCommon img {
  -moz-force-broken-image-icon: 1;
}

/* Restrict to direct children as other images could be nested in other content. */
.jp-RenderedHTMLCommon > img {
  display: block;
  margin-left: 0;
  margin-right: 0;
  margin-bottom: 1em;
}

/* Change color behind transparent images if they need it... */
[data-jp-theme-light='false'] .jp-RenderedImage img.jp-needs-light-background {
  background-color: var(--jp-inverse-layout-color1);
}
[data-jp-theme-light='true'] .jp-RenderedImage img.jp-needs-dark-background {
  background-color: var(--jp-inverse-layout-color1);
}
/* ...or leave it untouched if they don't */
[data-jp-theme-light='false'] .jp-RenderedImage img.jp-needs-dark-background {
}
[data-jp-theme-light='true'] .jp-RenderedImage img.jp-needs-light-background {
}

.jp-RenderedHTMLCommon img,
.jp-RenderedImage img,
.jp-RenderedHTMLCommon svg,
.jp-RenderedSVG svg {
  max-width: 100%;
  height: auto;
}

.jp-RenderedHTMLCommon img.jp-mod-unconfined,
.jp-RenderedImage img.jp-mod-unconfined,
.jp-RenderedHTMLCommon svg.jp-mod-unconfined,
.jp-RenderedSVG svg.jp-mod-unconfined {
  max-width: none;
}

.jp-RenderedHTMLCommon .alert {
  padding: var(--jp-notebook-padding);
  border: var(--jp-border-width) solid transparent;
  border-radius: var(--jp-border-radius);
  margin-bottom: 1em;
}

.jp-RenderedHTMLCommon .alert-info {
  color: var(--jp-info-color0);
  background-color: var(--jp-info-color3);
  border-color: var(--jp-info-color2);
}
.jp-RenderedHTMLCommon .alert-info hr {
  border-color: var(--jp-info-color3);
}
.jp-RenderedHTMLCommon .alert-info > p:last-child,
.jp-RenderedHTMLCommon .alert-info > ul:last-child {
  margin-bottom: 0;
}

.jp-RenderedHTMLCommon .alert-warning {
  color: var(--jp-warn-color0);
  background-color: var(--jp-warn-color3);
  border-color: var(--jp-warn-color2);
}
.jp-RenderedHTMLCommon .alert-warning hr {
  border-color: var(--jp-warn-color3);
}
.jp-RenderedHTMLCommon .alert-warning > p:last-child,
.jp-RenderedHTMLCommon .alert-warning > ul:last-child {
  margin-bottom: 0;
}

.jp-RenderedHTMLCommon .alert-success {
  color: var(--jp-success-color0);
  background-color: var(--jp-success-color3);
  border-color: var(--jp-success-color2);
}
.jp-RenderedHTMLCommon .alert-success hr {
  border-color: var(--jp-success-color3);
}
.jp-RenderedHTMLCommon .alert-success > p:last-child,
.jp-RenderedHTMLCommon .alert-success > ul:last-child {
  margin-bottom: 0;
}

.jp-RenderedHTMLCommon .alert-danger {
  color: var(--jp-error-color0);
  background-color: var(--jp-error-color3);
  border-color: var(--jp-error-color2);
}
.jp-RenderedHTMLCommon .alert-danger hr {
  border-color: var(--jp-error-color3);
}
.jp-RenderedHTMLCommon .alert-danger > p:last-child,
.jp-RenderedHTMLCommon .alert-danger > ul:last-child {
  margin-bottom: 0;
}

.jp-RenderedHTMLCommon blockquote {
  margin: 1em 2em;
  padding: 0 1em;
  border-left: 5px solid var(--jp-border-color2);
}

a.jp-InternalAnchorLink {
  visibility: hidden;
  margin-left: 8px;
  color: var(--md-blue-800);
}

h1:hover .jp-InternalAnchorLink,
h2:hover .jp-InternalAnchorLink,
h3:hover .jp-InternalAnchorLink,
h4:hover .jp-InternalAnchorLink,
h5:hover .jp-InternalAnchorLink,
h6:hover .jp-InternalAnchorLink {
  visibility: visible;
}

.jp-RenderedHTMLCommon kbd {
  background-color: var(--jp-rendermime-table-row-background);
  border: 1px solid var(--jp-border-color0);
  border-bottom-color: var(--jp-border-color2);
  border-radius: 3px;
  box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.25);
  display: inline-block;
  font-size: 0.8em;
  line-height: 1em;
  padding: 0.2em 0.5em;
}

/* Most direct children of .jp-RenderedHTMLCommon have a margin-bottom of 1.0.
 * At the bottom of cells this is a bit too much as there is also spacing
 * between cells. Going all the way to 0 gets too tight between markdown and
 * code cells.
 */
.jp-RenderedHTMLCommon > *:last-child {
  margin-bottom: 0.5em;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-MimeDocument {
  outline: none;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Variables
|----------------------------------------------------------------------------*/

:root {
  --jp-private-filebrowser-button-height: 28px;
  --jp-private-filebrowser-button-width: 48px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-FileBrowser {
  display: flex;
  flex-direction: column;
  color: var(--jp-ui-font-color1);
  background: var(--jp-layout-color1);
  /* This is needed so that all font sizing of children done in ems is
   * relative to this base size */
  font-size: var(--jp-ui-font-size1);
}

.jp-FileBrowser-toolbar.jp-Toolbar {
  border-bottom: none;
  height: auto;
  margin: var(--jp-toolbar-header-margin);
  box-shadow: none;
}

.jp-BreadCrumbs {
  flex: 0 0 auto;
  margin: 8px 12px 8px 12px;
}

.jp-BreadCrumbs-item {
  margin: 0px 2px;
  padding: 0px 2px;
  border-radius: var(--jp-border-radius);
  cursor: pointer;
}

.jp-BreadCrumbs-item:hover {
  background-color: var(--jp-layout-color2);
}

.jp-BreadCrumbs-item:first-child {
  margin-left: 0px;
}

.jp-BreadCrumbs-item.jp-mod-dropTarget {
  background-color: var(--jp-brand-color2);
  opacity: 0.7;
}

/*-----------------------------------------------------------------------------
| Buttons
|----------------------------------------------------------------------------*/

.jp-FileBrowser-toolbar.jp-Toolbar {
  padding: 0px;
  margin: 8px 12px 0px 12px;
}

.jp-FileBrowser-toolbar.jp-Toolbar {
  justify-content: flex-start;
}

.jp-FileBrowser-toolbar.jp-Toolbar .jp-Toolbar-item {
  flex: 0 0 auto;
  padding-left: 0px;
  padding-right: 2px;
}

.jp-FileBrowser-toolbar.jp-Toolbar .jp-ToolbarButtonComponent {
  width: 40px;
}

.jp-FileBrowser-toolbar.jp-Toolbar
  .jp-Toolbar-item:first-child
  .jp-ToolbarButtonComponent {
  width: 72px;
  background: var(--jp-brand-color1);
}

.jp-FileBrowser-toolbar.jp-Toolbar
  .jp-Toolbar-item:first-child
  .jp-ToolbarButtonComponent:focus-visible {
  background-color: var(--jp-brand-color0);
}

.jp-FileBrowser-toolbar.jp-Toolbar
  .jp-Toolbar-item:first-child
  .jp-ToolbarButtonComponent
  .jp-icon3 {
  fill: white;
}

/*-----------------------------------------------------------------------------
| Other styles
|----------------------------------------------------------------------------*/

.jp-FileDialog.jp-mod-conflict input {
  color: var(--jp-error-color1);
}

.jp-FileDialog .jp-new-name-title {
  margin-top: 12px;
}

.jp-LastModified-hidden {
  display: none;
}

.jp-FileBrowser-filterBox {
  padding: 0px;
  flex: 0 0 auto;
  margin: 8px 12px 0px 12px;
}

/*-----------------------------------------------------------------------------
| DirListing
|----------------------------------------------------------------------------*/

.jp-DirListing {
  flex: 1 1 auto;
  display: flex;
  flex-direction: column;
  outline: 0;
}

.jp-DirListing:focus-visible {
  border: 1px solid var(--jp-brand-color1);
}

.jp-DirListing-header {
  flex: 0 0 auto;
  display: flex;
  flex-direction: row;
  overflow: hidden;
  border-top: var(--jp-border-width) solid var(--jp-border-color2);
  border-bottom: var(--jp-border-width) solid var(--jp-border-color1);
  box-shadow: var(--jp-toolbar-box-shadow);
  z-index: 2;
}

.jp-DirListing-headerItem {
  padding: 4px 12px 2px 12px;
  font-weight: 500;
}

.jp-DirListing-headerItem:hover {
  background: var(--jp-layout-color2);
}

.jp-DirListing-headerItem.jp-id-name {
  flex: 1 0 84px;
}

.jp-DirListing-headerItem.jp-id-modified {
  flex: 0 0 112px;
  border-left: var(--jp-border-width) solid var(--jp-border-color2);
  text-align: right;
}

.jp-id-narrow {
  display: none;
  flex: 0 0 5px;
  padding: 4px 4px;
  border-left: var(--jp-border-width) solid var(--jp-border-color2);
  text-align: right;
  color: var(--jp-border-color2);
}

.jp-DirListing-narrow .jp-id-narrow {
  display: block;
}

.jp-DirListing-narrow .jp-id-modified,
.jp-DirListing-narrow .jp-DirListing-itemModified {
  display: none;
}

.jp-DirListing-headerItem.jp-mod-selected {
  font-weight: 600;
}

/* increase specificity to override bundled default */
.jp-DirListing-content {
  flex: 1 1 auto;
  margin: 0;
  padding: 0;
  list-style-type: none;
  overflow: auto;
  background-color: var(--jp-layout-color1);
}

.jp-DirListing-content mark {
  color: var(--jp-ui-font-color0);
  background-color: transparent;
  font-weight: bold;
}

.jp-DirListing-content .jp-DirListing-item.jp-mod-selected mark {
  color: var(--jp-ui-inverse-font-color0);
}

/* Style the directory listing content when a user drops a file to upload */
.jp-DirListing.jp-mod-native-drop .jp-DirListing-content {
  outline: 5px dashed rgba(128, 128, 128, 0.5);
  outline-offset: -10px;
  cursor: copy;
}

.jp-DirListing-item {
  display: flex;
  flex-direction: row;
  padding: 4px 12px;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

.jp-DirListing-item[data-is-dot] {
  opacity: 75%;
}

.jp-DirListing-item.jp-mod-selected {
  color: var(--jp-ui-inverse-font-color1);
  background: var(--jp-brand-color1);
}

.jp-DirListing-item.jp-mod-dropTarget {
  background: var(--jp-brand-color3);
}

.jp-DirListing-item:hover:not(.jp-mod-selected) {
  background: var(--jp-layout-color2);
}

.jp-DirListing-itemIcon {
  flex: 0 0 20px;
  margin-right: 4px;
}

.jp-DirListing-itemText {
  flex: 1 0 64px;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
  user-select: none;
}

.jp-DirListing-itemModified {
  flex: 0 0 125px;
  text-align: right;
}

.jp-DirListing-editor {
  flex: 1 0 64px;
  outline: none;
  border: none;
}

.jp-DirListing-item.jp-mod-running .jp-DirListing-itemIcon:before {
  color: var(--jp-success-color1);
  content: '\25CF';
  font-size: 8px;
  position: absolute;
  left: -8px;
}

.jp-DirListing-item.jp-mod-running.jp-mod-selected
  .jp-DirListing-itemIcon:before {
  color: var(--jp-ui-inverse-font-color1);
}

.jp-DirListing-item.lm-mod-drag-image,
.jp-DirListing-item.jp-mod-selected.lm-mod-drag-image {
  font-size: var(--jp-ui-font-size1);
  padding-left: 4px;
  margin-left: 4px;
  width: 160px;
  background-color: var(--jp-ui-inverse-font-color2);
  box-shadow: var(--jp-elevation-z2);
  border-radius: 0px;
  color: var(--jp-ui-font-color1);
  transform: translateX(-40%) translateY(-58%);
}

.jp-DirListing-deadSpace {
  flex: 1 1 auto;
  margin: 0;
  padding: 0;
  list-style-type: none;
  overflow: auto;
  background-color: var(--jp-layout-color1);
}

.jp-Document {
  min-width: 120px;
  min-height: 120px;
  outline: none;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Private CSS variables
|----------------------------------------------------------------------------*/

:root {
}

/*-----------------------------------------------------------------------------
| Main OutputArea
| OutputArea has a list of Outputs
|----------------------------------------------------------------------------*/

.jp-OutputArea {
  overflow-y: auto;
}

.jp-OutputArea-child {
  display: flex;
  flex-direction: row;
}

body[data-format='mobile'] .jp-OutputArea-child {
  flex-direction: column;
}

.jp-OutputPrompt {
  flex: 0 0 var(--jp-cell-prompt-width);
  color: var(--jp-cell-outprompt-font-color);
  font-family: var(--jp-cell-prompt-font-family);
  padding: var(--jp-code-padding);
  letter-spacing: var(--jp-cell-prompt-letter-spacing);
  line-height: var(--jp-code-line-height);
  font-size: var(--jp-code-font-size);
  border: var(--jp-border-width) solid transparent;
  opacity: var(--jp-cell-prompt-opacity);
  /* Right align prompt text, don't wrap to handle large prompt numbers */
  text-align: right;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
  /* Disable text selection */
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

body[data-format='mobile'] .jp-OutputPrompt {
  flex: 0 0 auto;
  text-align: left;
}

.jp-OutputArea-output {
  height: auto;
  overflow: auto;
  user-select: text;
  -moz-user-select: text;
  -webkit-user-select: text;
  -ms-user-select: text;
}

.jp-OutputArea-child .jp-OutputArea-output {
  flex-grow: 1;
  flex-shrink: 1;
}

body[data-format='mobile'] .jp-OutputArea-child .jp-OutputArea-output {
  margin-left: var(--jp-notebook-padding);
}

/**
 * Isolated output.
 */
.jp-OutputArea-output.jp-mod-isolated {
  width: 100%;
  display: block;
}

/*
When drag events occur, `p-mod-override-cursor` is added to the body.
Because iframes steal all cursor events, the following two rules are necessary
to suppress pointer events while resize drags are occurring. There may be a
better solution to this problem.
*/
body.lm-mod-override-cursor .jp-OutputArea-output.jp-mod-isolated {
  position: relative;
}

body.lm-mod-override-cursor .jp-OutputArea-output.jp-mod-isolated:before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: transparent;
}

/* pre */

.jp-OutputArea-output pre {
  border: none;
  margin: 0px;
  padding: 0px;
  overflow-x: auto;
  overflow-y: auto;
  word-break: break-all;
  word-wrap: break-word;
  white-space: pre-wrap;
}

/* tables */

.jp-OutputArea-output.jp-RenderedHTMLCommon table {
  margin-left: 0;
  margin-right: 0;
}

/* description lists */

.jp-OutputArea-output dl,
.jp-OutputArea-output dt,
.jp-OutputArea-output dd {
  display: block;
}

.jp-OutputArea-output dl {
  width: 100%;
  overflow: hidden;
  padding: 0;
  margin: 0;
}

.jp-OutputArea-output dt {
  font-weight: bold;
  float: left;
  width: 20%;
  padding: 0;
  margin: 0;
}

.jp-OutputArea-output dd {
  float: left;
  width: 80%;
  padding: 0;
  margin: 0;
}

/* Hide the gutter in case of
 *  - nested output areas (e.g. in the case of output widgets)
 *  - mirrored output areas
 */
.jp-OutputArea .jp-OutputArea .jp-OutputArea-prompt {
  display: none;
}

/*-----------------------------------------------------------------------------
| executeResult is added to any Output-result for the display of the object
| returned by a cell
|----------------------------------------------------------------------------*/

.jp-OutputArea-output.jp-OutputArea-executeResult {
  margin-left: 0px;
  flex: 1 1 auto;
}

/* Text output with the Out[] prompt needs a top padding to match the
 * alignment of the Out[] prompt itself.
 */
.jp-OutputArea-executeResult .jp-RenderedText.jp-OutputArea-output {
  padding-top: var(--jp-code-padding);
  border-top: var(--jp-border-width) solid transparent;
}

/*-----------------------------------------------------------------------------
| The Stdin output
|----------------------------------------------------------------------------*/

.jp-OutputArea-stdin {
  line-height: var(--jp-code-line-height);
  padding-top: var(--jp-code-padding);
  display: flex;
}

.jp-Stdin-prompt {
  color: var(--jp-content-font-color0);
  padding-right: var(--jp-code-padding);
  vertical-align: baseline;
  flex: 0 0 auto;
}

.jp-Stdin-input {
  font-family: var(--jp-code-font-family);
  font-size: inherit;
  color: inherit;
  background-color: inherit;
  width: 42%;
  min-width: 200px;
  /* make sure input baseline aligns with prompt */
  vertical-align: baseline;
  /* padding + margin = 0.5em between prompt and cursor */
  padding: 0em 0.25em;
  margin: 0em 0.25em;
  flex: 0 0 70%;
}

.jp-Stdin-input:focus {
  box-shadow: none;
}

/*-----------------------------------------------------------------------------
| Output Area View
|----------------------------------------------------------------------------*/

.jp-LinkedOutputView .jp-OutputArea {
  height: 100%;
  display: block;
}

.jp-LinkedOutputView .jp-OutputArea-output:only-child {
  height: 100%;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-Collapser {
  flex: 0 0 var(--jp-cell-collapser-width);
  padding: 0px;
  margin: 0px;
  border: none;
  outline: none;
  background: transparent;
  border-radius: var(--jp-border-radius);
  opacity: 1;
}

.jp-Collapser-child {
  display: block;
  width: 100%;
  box-sizing: border-box;
  /* height: 100% doesn't work because the height of its parent is computed from content */
  position: absolute;
  top: 0px;
  bottom: 0px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Header/Footer
|----------------------------------------------------------------------------*/

/* Hidden by zero height by default */
.jp-CellHeader,
.jp-CellFooter {
  height: 0px;
  width: 100%;
  padding: 0px;
  margin: 0px;
  border: none;
  outline: none;
  background: transparent;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Input
|----------------------------------------------------------------------------*/

/* All input areas */
.jp-InputArea {
  display: flex;
  flex-direction: row;
  overflow: hidden;
}

body[data-format='mobile'] .jp-InputArea {
  flex-direction: column;
}

.jp-InputArea-editor {
  flex: 1 1 auto;
  overflow: hidden;
}

.jp-InputArea-editor {
  /* This is the non-active, default styling */
  border: var(--jp-border-width) solid var(--jp-cell-editor-border-color);
  border-radius: 0px;
  background: var(--jp-cell-editor-background);
}

body[data-format='mobile'] .jp-InputArea-editor {
  margin-left: var(--jp-notebook-padding);
}

.jp-InputPrompt {
  flex: 0 0 var(--jp-cell-prompt-width);
  color: var(--jp-cell-inprompt-font-color);
  font-family: var(--jp-cell-prompt-font-family);
  padding: var(--jp-code-padding);
  letter-spacing: var(--jp-cell-prompt-letter-spacing);
  opacity: var(--jp-cell-prompt-opacity);
  line-height: var(--jp-code-line-height);
  font-size: var(--jp-code-font-size);
  border: var(--jp-border-width) solid transparent;
  opacity: var(--jp-cell-prompt-opacity);
  /* Right align prompt text, don't wrap to handle large prompt numbers */
  text-align: right;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
  /* Disable text selection */
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

body[data-format='mobile'] .jp-InputPrompt {
  flex: 0 0 auto;
  text-align: left;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Placeholder
|----------------------------------------------------------------------------*/

.jp-Placeholder {
  display: flex;
  flex-direction: row;
  flex: 1 1 auto;
}

.jp-Placeholder-prompt {
  box-sizing: border-box;
}

.jp-Placeholder-content {
  flex: 1 1 auto;
  border: none;
  background: transparent;
  height: 20px;
  box-sizing: border-box;
}

.jp-Placeholder-content .jp-MoreHorizIcon {
  width: 32px;
  height: 16px;
  border: 1px solid transparent;
  border-radius: var(--jp-border-radius);
}

.jp-Placeholder-content .jp-MoreHorizIcon:hover {
  border: 1px solid var(--jp-border-color1);
  box-shadow: 0px 0px 2px 0px rgba(0, 0, 0, 0.25);
  background-color: var(--jp-layout-color0);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Private CSS variables
|----------------------------------------------------------------------------*/

:root {
  --jp-private-cell-scrolling-output-offset: 5px;
}

/*-----------------------------------------------------------------------------
| Cell
|----------------------------------------------------------------------------*/

.jp-Cell {
  padding: var(--jp-cell-padding);
  margin: 0px;
  border: none;
  outline: none;
  background: transparent;
}

/*-----------------------------------------------------------------------------
| Common input/output
|----------------------------------------------------------------------------*/

.jp-Cell-inputWrapper,
.jp-Cell-outputWrapper {
  display: flex;
  flex-direction: row;
  padding: 0px;
  margin: 0px;
  /* Added to reveal the box-shadow on the input and output collapsers. */
  overflow: visible;
}

/* Only input/output areas inside cells */
.jp-Cell-inputArea,
.jp-Cell-outputArea {
  flex: 1 1 auto;
}

/*-----------------------------------------------------------------------------
| Collapser
|----------------------------------------------------------------------------*/

/* Make the output collapser disappear when there is not output, but do so
 * in a manner that leaves it in the layout and preserves its width.
 */
.jp-Cell.jp-mod-noOutputs .jp-Cell-outputCollapser {
  border: none !important;
  background: transparent !important;
}

.jp-Cell:not(.jp-mod-noOutputs) .jp-Cell-outputCollapser {
  min-height: var(--jp-cell-collapser-min-height);
}

/*-----------------------------------------------------------------------------
| Output
|----------------------------------------------------------------------------*/

/* Put a space between input and output when there IS output */
.jp-Cell:not(.jp-mod-noOutputs) .jp-Cell-outputWrapper {
  margin-top: 5px;
}

.jp-CodeCell.jp-mod-outputsScrolled .jp-Cell-outputArea {
  overflow-y: auto;
  max-height: 200px;
  box-shadow: inset 0 0 6px 2px rgba(0, 0, 0, 0.3);
  margin-left: var(--jp-private-cell-scrolling-output-offset);
}

.jp-CodeCell.jp-mod-outputsScrolled .jp-OutputArea-prompt {
  flex: 0 0
    calc(
      var(--jp-cell-prompt-width) -
        var(--jp-private-cell-scrolling-output-offset)
    );
}

/*-----------------------------------------------------------------------------
| CodeCell
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| MarkdownCell
|----------------------------------------------------------------------------*/

.jp-MarkdownOutput {
  flex: 1 1 auto;
  margin-top: 0;
  margin-bottom: 0;
  padding-left: var(--jp-code-padding);
}

.jp-MarkdownOutput.jp-RenderedHTMLCommon {
  overflow: auto;
}

.jp-showHiddenCellsButton {
  margin-left: calc(var(--jp-cell-prompt-width) + 2 * var(--jp-code-padding));
  margin-top: var(--jp-code-padding);
  border: 1px solid var(--jp-border-color2);
  background-color: var(--jp-border-color3) !important;
  color: var(--jp-content-font-color0) !important;
}

.jp-showHiddenCellsButton:hover {
  background-color: var(--jp-border-color2) !important;
}

.jp-collapseHeadingButton {
  display: none;
}

.jp-MarkdownCell:hover .jp-collapseHeadingButton {
  display: flex;
  min-height: var(--jp-cell-collapser-min-height);
  position: absolute;
  right: 0;
  top: 0;
  bottom: 0;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Variables
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------

/*-----------------------------------------------------------------------------
| Styles
|----------------------------------------------------------------------------*/

.jp-NotebookPanel-toolbar {
  padding: 2px;
}

.jp-Toolbar-item.jp-Notebook-toolbarCellType .jp-select-wrapper.jp-mod-focused {
  border: none;
  box-shadow: none;
}

.jp-Notebook-toolbarCellTypeDropdown select {
  height: 24px;
  font-size: var(--jp-ui-font-size1);
  line-height: 14px;
  border-radius: 0;
  display: block;
}

.jp-Notebook-toolbarCellTypeDropdown span {
  top: 5px !important;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Private CSS variables
|----------------------------------------------------------------------------*/

:root {
  --jp-private-notebook-dragImage-width: 304px;
  --jp-private-notebook-dragImage-height: 36px;
  --jp-private-notebook-selected-color: var(--md-blue-400);
  --jp-private-notebook-active-color: var(--md-green-400);
}

/*-----------------------------------------------------------------------------
| Imports
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Notebook
|----------------------------------------------------------------------------*/

.jp-NotebookPanel {
  display: block;
  height: 100%;
}

.jp-NotebookPanel.jp-Document {
  min-width: 240px;
  min-height: 120px;
}

.jp-Notebook {
  padding: var(--jp-notebook-padding);
  outline: none;
  overflow: auto;
  background: var(--jp-layout-color0);
}

.jp-Notebook.jp-mod-scrollPastEnd::after {
  display: block;
  content: '';
  min-height: var(--jp-notebook-scroll-padding);
}

.jp-MainAreaWidget-ContainStrict .jp-Notebook * {
  contain: strict;
}

.jp-Notebook-render * {
  contain: none !important;
}

.jp-Notebook .jp-Cell {
  overflow: visible;
}

.jp-Notebook .jp-Cell .jp-InputPrompt {
  cursor: move;
  float: left;
}

/*-----------------------------------------------------------------------------
| Notebook state related styling
|
| The notebook and cells each have states, here are the possibilities:
|
| - Notebook
|   - Command
|   - Edit
| - Cell
|   - None
|   - Active (only one can be active)
|   - Selected (the cells actions are applied to)
|   - Multiselected (when multiple selected, the cursor)
|   - No outputs
|----------------------------------------------------------------------------*/

/* Command or edit modes */

.jp-Notebook .jp-Cell:not(.jp-mod-active) .jp-InputPrompt {
  opacity: var(--jp-cell-prompt-not-active-opacity);
  color: var(--jp-cell-prompt-not-active-font-color);
}

.jp-Notebook .jp-Cell:not(.jp-mod-active) .jp-OutputPrompt {
  opacity: var(--jp-cell-prompt-not-active-opacity);
  color: var(--jp-cell-prompt-not-active-font-color);
}

/* cell is active */
.jp-Notebook .jp-Cell.jp-mod-active .jp-Collapser {
  background: var(--jp-brand-color1);
}

/* cell is dirty */
.jp-Notebook .jp-Cell.jp-mod-dirty .jp-InputPrompt {
  color: var(--jp-warn-color1);
}
.jp-Notebook .jp-Cell.jp-mod-dirty .jp-InputPrompt:before {
  color: var(--jp-warn-color1);
  content: '•';
}

.jp-Notebook .jp-Cell.jp-mod-active.jp-mod-dirty .jp-Collapser {
  background: var(--jp-warn-color1);
}

/* collapser is hovered */
.jp-Notebook .jp-Cell .jp-Collapser:hover {
  box-shadow: var(--jp-elevation-z2);
  background: var(--jp-brand-color1);
  opacity: var(--jp-cell-collapser-not-active-hover-opacity);
}

/* cell is active and collapser is hovered */
.jp-Notebook .jp-Cell.jp-mod-active .jp-Collapser:hover {
  background: var(--jp-brand-color0);
  opacity: 1;
}

/* Command mode */

.jp-Notebook.jp-mod-commandMode .jp-Cell.jp-mod-selected {
  background: var(--jp-notebook-multiselected-color);
}

.jp-Notebook.jp-mod-commandMode
  .jp-Cell.jp-mod-active.jp-mod-selected:not(.jp-mod-multiSelected) {
  background: transparent;
}

/* Edit mode */

.jp-Notebook.jp-mod-editMode .jp-Cell.jp-mod-active .jp-InputArea-editor {
  border: var(--jp-border-width) solid var(--jp-cell-editor-active-border-color);
  box-shadow: var(--jp-input-box-shadow);
  background-color: var(--jp-cell-editor-active-background);
}

/*-----------------------------------------------------------------------------
| Notebook drag and drop
|----------------------------------------------------------------------------*/

.jp-Notebook-cell.jp-mod-dropSource {
  opacity: 0.5;
}

.jp-Notebook-cell.jp-mod-dropTarget,
.jp-Notebook.jp-mod-commandMode
  .jp-Notebook-cell.jp-mod-active.jp-mod-selected.jp-mod-dropTarget {
  border-top-color: var(--jp-private-notebook-selected-color);
  border-top-style: solid;
  border-top-width: 2px;
}

.jp-dragImage {
  display: block;
  flex-direction: row;
  width: var(--jp-private-notebook-dragImage-width);
  height: var(--jp-private-notebook-dragImage-height);
  border: var(--jp-border-width) solid var(--jp-cell-editor-border-color);
  background: var(--jp-cell-editor-background);
  overflow: visible;
}

.jp-dragImage-singlePrompt {
  box-shadow: 2px 2px 4px 0px rgba(0, 0, 0, 0.12);
}

.jp-dragImage .jp-dragImage-content {
  flex: 1 1 auto;
  z-index: 2;
  font-size: var(--jp-code-font-size);
  font-family: var(--jp-code-font-family);
  line-height: var(--jp-code-line-height);
  padding: var(--jp-code-padding);
  border: var(--jp-border-width) solid var(--jp-cell-editor-border-color);
  background: var(--jp-cell-editor-background-color);
  color: var(--jp-content-font-color3);
  text-align: left;
  margin: 4px 4px 4px 0px;
}

.jp-dragImage .jp-dragImage-prompt {
  flex: 0 0 auto;
  min-width: 36px;
  color: var(--jp-cell-inprompt-font-color);
  padding: var(--jp-code-padding);
  padding-left: 12px;
  font-family: var(--jp-cell-prompt-font-family);
  letter-spacing: var(--jp-cell-prompt-letter-spacing);
  line-height: 1.9;
  font-size: var(--jp-code-font-size);
  border: var(--jp-border-width) solid transparent;
}

.jp-dragImage-multipleBack {
  z-index: -1;
  position: absolute;
  height: 32px;
  width: 300px;
  top: 8px;
  left: 8px;
  background: var(--jp-layout-color2);
  border: var(--jp-border-width) solid var(--jp-input-border-color);
  box-shadow: 2px 2px 4px 0px rgba(0, 0, 0, 0.12);
}

/*-----------------------------------------------------------------------------
| Cell toolbar
|----------------------------------------------------------------------------*/

.jp-NotebookTools {
  display: block;
  min-width: var(--jp-sidebar-min-width);
  color: var(--jp-ui-font-color1);
  background: var(--jp-layout-color1);
  /* This is needed so that all font sizing of children done in ems is
    * relative to this base size */
  font-size: var(--jp-ui-font-size1);
  overflow: auto;
}

.jp-NotebookTools-tool {
  padding: 0px 12px 0 12px;
}

.jp-ActiveCellTool {
  padding: 12px;
  background-color: var(--jp-layout-color1);
  border-top: none !important;
}

.jp-ActiveCellTool .jp-InputArea-prompt {
  flex: 0 0 auto;
  padding-left: 0px;
}

.jp-ActiveCellTool .jp-InputArea-editor {
  flex: 1 1 auto;
  background: var(--jp-cell-editor-background);
  border-color: var(--jp-cell-editor-border-color);
}

.jp-ActiveCellTool .jp-InputArea-editor .CodeMirror {
  background: transparent;
}

.jp-MetadataEditorTool {
  flex-direction: column;
  padding: 12px 0px 12px 0px;
}

.jp-RankedPanel > :not(:first-child) {
  margin-top: 12px;
}

.jp-KeySelector select.jp-mod-styled {
  font-size: var(--jp-ui-font-size1);
  color: var(--jp-ui-font-color0);
  border: var(--jp-border-width) solid var(--jp-border-color1);
}

.jp-KeySelector label,
.jp-MetadataEditorTool label {
  line-height: 1.4;
}

.jp-NotebookTools .jp-select-wrapper {
  margin-top: 4px;
  margin-bottom: 0px;
}

.jp-NotebookTools .jp-Collapse {
  margin-top: 16px;
}

/*-----------------------------------------------------------------------------
| Presentation Mode (.jp-mod-presentationMode)
|----------------------------------------------------------------------------*/

.jp-mod-presentationMode .jp-Notebook {
  --jp-content-font-size1: var(--jp-content-presentation-font-size1);
  --jp-code-font-size: var(--jp-code-presentation-font-size);
}

.jp-mod-presentationMode .jp-Notebook .jp-Cell .jp-InputPrompt,
.jp-mod-presentationMode .jp-Notebook .jp-Cell .jp-OutputPrompt {
  flex: 0 0 110px;
}

/*-----------------------------------------------------------------------------
| Placeholder
|----------------------------------------------------------------------------*/

.jp-Cell-Placeholder {
  padding-left: 55px;
}

.jp-Cell-Placeholder-wrapper {
  background: #fff;
  border: 1px solid;
  border-color: #e5e6e9 #dfe0e4 #d0d1d5;
  border-radius: 4px;
  -webkit-border-radius: 4px;
  margin: 10px 15px;
}

.jp-Cell-Placeholder-wrapper-inner {
  padding: 15px;
  position: relative;
}

.jp-Cell-Placeholder-wrapper-body {
  background-repeat: repeat;
  background-size: 50% auto;
}

.jp-Cell-Placeholder-wrapper-body div {
  background: #f6f7f8;
  background-image: -webkit-linear-gradient(
    left,
    #f6f7f8 0%,
    #edeef1 20%,
    #f6f7f8 40%,
    #f6f7f8 100%
  );
  background-repeat: no-repeat;
  background-size: 800px 104px;
  height: 104px;
  position: relative;
}

.jp-Cell-Placeholder-wrapper-body div {
  position: absolute;
  right: 15px;
  left: 15px;
  top: 15px;
}

div.jp-Cell-Placeholder-h1 {
  top: 20px;
  height: 20px;
  left: 15px;
  width: 150px;
}

div.jp-Cell-Placeholder-h2 {
  left: 15px;
  top: 50px;
  height: 10px;
  width: 100px;
}

div.jp-Cell-Placeholder-content-1,
div.jp-Cell-Placeholder-content-2,
div.jp-Cell-Placeholder-content-3 {
  left: 15px;
  right: 15px;
  height: 10px;
}

div.jp-Cell-Placeholder-content-1 {
  top: 100px;
}

div.jp-Cell-Placeholder-content-2 {
  top: 120px;
}

div.jp-Cell-Placeholder-content-3 {
  top: 140px;
}

</style>

    <style type="text/css">
/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*
The following CSS variables define the main, public API for styling JupyterLab.
These variables should be used by all plugins wherever possible. In other
words, plugins should not define custom colors, sizes, etc unless absolutely
necessary. This enables users to change the visual theme of JupyterLab
by changing these variables.

Many variables appear in an ordered sequence (0,1,2,3). These sequences
are designed to work well together, so for example, `--jp-border-color1` should
be used with `--jp-layout-color1`. The numbers have the following meanings:

* 0: super-primary, reserved for special emphasis
* 1: primary, most important under normal situations
* 2: secondary, next most important under normal situations
* 3: tertiary, next most important under normal situations

Throughout JupyterLab, we are mostly following principles from Google's
Material Design when selecting colors. We are not, however, following
all of MD as it is not optimized for dense, information rich UIs.
*/

:root {
  /* Elevation
   *
   * We style box-shadows using Material Design's idea of elevation. These particular numbers are taken from here:
   *
   * https://github.com/material-components/material-components-web
   * https://material-components-web.appspot.com/elevation.html
   */

  --jp-shadow-base-lightness: 0;
  --jp-shadow-umbra-color: rgba(
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    0.2
  );
  --jp-shadow-penumbra-color: rgba(
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    0.14
  );
  --jp-shadow-ambient-color: rgba(
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    0.12
  );
  --jp-elevation-z0: none;
  --jp-elevation-z1: 0px 2px 1px -1px var(--jp-shadow-umbra-color),
    0px 1px 1px 0px var(--jp-shadow-penumbra-color),
    0px 1px 3px 0px var(--jp-shadow-ambient-color);
  --jp-elevation-z2: 0px 3px 1px -2px var(--jp-shadow-umbra-color),
    0px 2px 2px 0px var(--jp-shadow-penumbra-color),
    0px 1px 5px 0px var(--jp-shadow-ambient-color);
  --jp-elevation-z4: 0px 2px 4px -1px var(--jp-shadow-umbra-color),
    0px 4px 5px 0px var(--jp-shadow-penumbra-color),
    0px 1px 10px 0px var(--jp-shadow-ambient-color);
  --jp-elevation-z6: 0px 3px 5px -1px var(--jp-shadow-umbra-color),
    0px 6px 10px 0px var(--jp-shadow-penumbra-color),
    0px 1px 18px 0px var(--jp-shadow-ambient-color);
  --jp-elevation-z8: 0px 5px 5px -3px var(--jp-shadow-umbra-color),
    0px 8px 10px 1px var(--jp-shadow-penumbra-color),
    0px 3px 14px 2px var(--jp-shadow-ambient-color);
  --jp-elevation-z12: 0px 7px 8px -4px var(--jp-shadow-umbra-color),
    0px 12px 17px 2px var(--jp-shadow-penumbra-color),
    0px 5px 22px 4px var(--jp-shadow-ambient-color);
  --jp-elevation-z16: 0px 8px 10px -5px var(--jp-shadow-umbra-color),
    0px 16px 24px 2px var(--jp-shadow-penumbra-color),
    0px 6px 30px 5px var(--jp-shadow-ambient-color);
  --jp-elevation-z20: 0px 10px 13px -6px var(--jp-shadow-umbra-color),
    0px 20px 31px 3px var(--jp-shadow-penumbra-color),
    0px 8px 38px 7px var(--jp-shadow-ambient-color);
  --jp-elevation-z24: 0px 11px 15px -7px var(--jp-shadow-umbra-color),
    0px 24px 38px 3px var(--jp-shadow-penumbra-color),
    0px 9px 46px 8px var(--jp-shadow-ambient-color);

  /* Borders
   *
   * The following variables, specify the visual styling of borders in JupyterLab.
   */

  --jp-border-width: 1px;
  --jp-border-color0: var(--md-grey-400);
  --jp-border-color1: var(--md-grey-400);
  --jp-border-color2: var(--md-grey-300);
  --jp-border-color3: var(--md-grey-200);
  --jp-border-radius: 2px;

  /* UI Fonts
   *
   * The UI font CSS variables are used for the typography all of the JupyterLab
   * user interface elements that are not directly user generated content.
   *
   * The font sizing here is done assuming that the body font size of --jp-ui-font-size1
   * is applied to a parent element. When children elements, such as headings, are sized
   * in em all things will be computed relative to that body size.
   */

  --jp-ui-font-scale-factor: 1.2;
  --jp-ui-font-size0: 0.83333em;
  --jp-ui-font-size1: 13px; /* Base font size */
  --jp-ui-font-size2: 1.2em;
  --jp-ui-font-size3: 1.44em;

  --jp-ui-font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Helvetica,
    Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji', 'Segoe UI Symbol';

  /*
   * Use these font colors against the corresponding main layout colors.
   * In a light theme, these go from dark to light.
   */

  /* Defaults use Material Design specification */
  --jp-ui-font-color0: rgba(0, 0, 0, 1);
  --jp-ui-font-color1: rgba(0, 0, 0, 0.87);
  --jp-ui-font-color2: rgba(0, 0, 0, 0.54);
  --jp-ui-font-color3: rgba(0, 0, 0, 0.38);

  /*
   * Use these against the brand/accent/warn/error colors.
   * These will typically go from light to darker, in both a dark and light theme.
   */

  --jp-ui-inverse-font-color0: rgba(255, 255, 255, 1);
  --jp-ui-inverse-font-color1: rgba(255, 255, 255, 1);
  --jp-ui-inverse-font-color2: rgba(255, 255, 255, 0.7);
  --jp-ui-inverse-font-color3: rgba(255, 255, 255, 0.5);

  /* Content Fonts
   *
   * Content font variables are used for typography of user generated content.
   *
   * The font sizing here is done assuming that the body font size of --jp-content-font-size1
   * is applied to a parent element. When children elements, such as headings, are sized
   * in em all things will be computed relative to that body size.
   */

  --jp-content-line-height: 1.6;
  --jp-content-font-scale-factor: 1.2;
  --jp-content-font-size0: 0.83333em;
  --jp-content-font-size1: 14px; /* Base font size */
  --jp-content-font-size2: 1.2em;
  --jp-content-font-size3: 1.44em;
  --jp-content-font-size4: 1.728em;
  --jp-content-font-size5: 2.0736em;

  /* This gives a magnification of about 125% in presentation mode over normal. */
  --jp-content-presentation-font-size1: 17px;

  --jp-content-heading-line-height: 1;
  --jp-content-heading-margin-top: 1.2em;
  --jp-content-heading-margin-bottom: 0.8em;
  --jp-content-heading-font-weight: 500;

  /* Defaults use Material Design specification */
  --jp-content-font-color0: rgba(0, 0, 0, 1);
  --jp-content-font-color1: rgba(0, 0, 0, 0.87);
  --jp-content-font-color2: rgba(0, 0, 0, 0.54);
  --jp-content-font-color3: rgba(0, 0, 0, 0.38);

  --jp-content-link-color: var(--md-blue-700);

  --jp-content-font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Helvetica, Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji',
    'Segoe UI Symbol';

  /*
   * Code Fonts
   *
   * Code font variables are used for typography of code and other monospaces content.
   */

  --jp-code-font-size: 13px;
  --jp-code-line-height: 1.3077; /* 17px for 13px base */
  --jp-code-padding: 5px; /* 5px for 13px base, codemirror highlighting needs integer px value */
  --jp-code-font-family-default: Menlo, Consolas, 'DejaVu Sans Mono', monospace;
  --jp-code-font-family: var(--jp-code-font-family-default);

  /* This gives a magnification of about 125% in presentation mode over normal. */
  --jp-code-presentation-font-size: 16px;

  /* may need to tweak cursor width if you change font size */
  --jp-code-cursor-width0: 1.4px;
  --jp-code-cursor-width1: 2px;
  --jp-code-cursor-width2: 4px;

  /* Layout
   *
   * The following are the main layout colors use in JupyterLab. In a light
   * theme these would go from light to dark.
   */

  --jp-layout-color0: white;
  --jp-layout-color1: white;
  --jp-layout-color2: var(--md-grey-200);
  --jp-layout-color3: var(--md-grey-400);
  --jp-layout-color4: var(--md-grey-600);

  /* Inverse Layout
   *
   * The following are the inverse layout colors use in JupyterLab. In a light
   * theme these would go from dark to light.
   */

  --jp-inverse-layout-color0: #111111;
  --jp-inverse-layout-color1: var(--md-grey-900);
  --jp-inverse-layout-color2: var(--md-grey-800);
  --jp-inverse-layout-color3: var(--md-grey-700);
  --jp-inverse-layout-color4: var(--md-grey-600);

  /* Brand/accent */

  --jp-brand-color0: var(--md-blue-900);
  --jp-brand-color1: var(--md-blue-700);
  --jp-brand-color2: var(--md-blue-300);
  --jp-brand-color3: var(--md-blue-100);
  --jp-brand-color4: var(--md-blue-50);

  --jp-accent-color0: var(--md-green-900);
  --jp-accent-color1: var(--md-green-700);
  --jp-accent-color2: var(--md-green-300);
  --jp-accent-color3: var(--md-green-100);

  /* State colors (warn, error, success, info) */

  --jp-warn-color0: var(--md-orange-900);
  --jp-warn-color1: var(--md-orange-700);
  --jp-warn-color2: var(--md-orange-300);
  --jp-warn-color3: var(--md-orange-100);

  --jp-error-color0: var(--md-red-900);
  --jp-error-color1: var(--md-red-700);
  --jp-error-color2: var(--md-red-300);
  --jp-error-color3: var(--md-red-100);

  --jp-success-color0: var(--md-green-900);
  --jp-success-color1: var(--md-green-700);
  --jp-success-color2: var(--md-green-300);
  --jp-success-color3: var(--md-green-100);

  --jp-info-color0: var(--md-cyan-900);
  --jp-info-color1: var(--md-cyan-700);
  --jp-info-color2: var(--md-cyan-300);
  --jp-info-color3: var(--md-cyan-100);

  /* Cell specific styles */

  --jp-cell-padding: 5px;

  --jp-cell-collapser-width: 8px;
  --jp-cell-collapser-min-height: 20px;
  --jp-cell-collapser-not-active-hover-opacity: 0.6;

  --jp-cell-editor-background: var(--md-grey-100);
  --jp-cell-editor-border-color: var(--md-grey-300);
  --jp-cell-editor-box-shadow: inset 0 0 2px var(--md-blue-300);
  --jp-cell-editor-active-background: var(--jp-layout-color0);
  --jp-cell-editor-active-border-color: var(--jp-brand-color1);

  --jp-cell-prompt-width: 64px;
  --jp-cell-prompt-font-family: var(--jp-code-font-family-default);
  --jp-cell-prompt-letter-spacing: 0px;
  --jp-cell-prompt-opacity: 1;
  --jp-cell-prompt-not-active-opacity: 0.5;
  --jp-cell-prompt-not-active-font-color: var(--md-grey-700);
  /* A custom blend of MD grey and blue 600
   * See https://meyerweb.com/eric/tools/color-blend/#546E7A:1E88E5:5:hex */
  --jp-cell-inprompt-font-color: #307fc1;
  /* A custom blend of MD grey and orange 600
   * https://meyerweb.com/eric/tools/color-blend/#546E7A:F4511E:5:hex */
  --jp-cell-outprompt-font-color: #bf5b3d;

  /* Notebook specific styles */

  --jp-notebook-padding: 10px;
  --jp-notebook-select-background: var(--jp-layout-color1);
  --jp-notebook-multiselected-color: var(--md-blue-50);

  /* The scroll padding is calculated to fill enough space at the bottom of the
  notebook to show one single-line cell (with appropriate padding) at the top
  when the notebook is scrolled all the way to the bottom. We also subtract one
  pixel so that no scrollbar appears if we have just one single-line cell in the
  notebook. This padding is to enable a 'scroll past end' feature in a notebook.
  */
  --jp-notebook-scroll-padding: calc(
    100% - var(--jp-code-font-size) * var(--jp-code-line-height) -
      var(--jp-code-padding) - var(--jp-cell-padding) - 1px
  );

  /* Rendermime styles */

  --jp-rendermime-error-background: #fdd;
  --jp-rendermime-table-row-background: var(--md-grey-100);
  --jp-rendermime-table-row-hover-background: var(--md-light-blue-50);

  /* Dialog specific styles */

  --jp-dialog-background: rgba(0, 0, 0, 0.25);

  /* Console specific styles */

  --jp-console-padding: 10px;

  /* Toolbar specific styles */

  --jp-toolbar-border-color: var(--jp-border-color1);
  --jp-toolbar-micro-height: 8px;
  --jp-toolbar-background: var(--jp-layout-color1);
  --jp-toolbar-box-shadow: 0px 0px 2px 0px rgba(0, 0, 0, 0.24);
  --jp-toolbar-header-margin: 4px 4px 0px 4px;
  --jp-toolbar-active-background: var(--md-grey-300);

  /* Statusbar specific styles */

  --jp-statusbar-height: 24px;

  /* Input field styles */

  --jp-input-box-shadow: inset 0 0 2px var(--md-blue-300);
  --jp-input-active-background: var(--jp-layout-color1);
  --jp-input-hover-background: var(--jp-layout-color1);
  --jp-input-background: var(--md-grey-100);
  --jp-input-border-color: var(--jp-border-color1);
  --jp-input-active-border-color: var(--jp-brand-color1);
  --jp-input-active-box-shadow-color: rgba(19, 124, 189, 0.3);

  /* General editor styles */

  --jp-editor-selected-background: #d9d9d9;
  --jp-editor-selected-focused-background: #d7d4f0;
  --jp-editor-cursor-color: var(--jp-ui-font-color0);

  /* Code mirror specific styles */

  --jp-mirror-editor-keyword-color: #008000;
  --jp-mirror-editor-atom-color: #88f;
  --jp-mirror-editor-number-color: #080;
  --jp-mirror-editor-def-color: #00f;
  --jp-mirror-editor-variable-color: var(--md-grey-900);
  --jp-mirror-editor-variable-2-color: #05a;
  --jp-mirror-editor-variable-3-color: #085;
  --jp-mirror-editor-punctuation-color: #05a;
  --jp-mirror-editor-property-color: #05a;
  --jp-mirror-editor-operator-color: #aa22ff;
  --jp-mirror-editor-comment-color: #408080;
  --jp-mirror-editor-string-color: #ba2121;
  --jp-mirror-editor-string-2-color: #708;
  --jp-mirror-editor-meta-color: #aa22ff;
  --jp-mirror-editor-qualifier-color: #555;
  --jp-mirror-editor-builtin-color: #008000;
  --jp-mirror-editor-bracket-color: #997;
  --jp-mirror-editor-tag-color: #170;
  --jp-mirror-editor-attribute-color: #00c;
  --jp-mirror-editor-header-color: blue;
  --jp-mirror-editor-quote-color: #090;
  --jp-mirror-editor-link-color: #00c;
  --jp-mirror-editor-error-color: #f00;
  --jp-mirror-editor-hr-color: #999;

  /* Vega extension styles */

  --jp-vega-background: white;

  /* Sidebar-related styles */

  --jp-sidebar-min-width: 250px;

  /* Search-related styles */

  --jp-search-toggle-off-opacity: 0.5;
  --jp-search-toggle-hover-opacity: 0.8;
  --jp-search-toggle-on-opacity: 1;
  --jp-search-selected-match-background-color: rgb(245, 200, 0);
  --jp-search-selected-match-color: black;
  --jp-search-unselected-match-background-color: var(
    --jp-inverse-layout-color0
  );
  --jp-search-unselected-match-color: var(--jp-ui-inverse-font-color0);

  /* Icon colors that work well with light or dark backgrounds */
  --jp-icon-contrast-color0: var(--md-purple-600);
  --jp-icon-contrast-color1: var(--md-green-600);
  --jp-icon-contrast-color2: var(--md-pink-600);
  --jp-icon-contrast-color3: var(--md-blue-600);
}
</style>

<style type="text/css">
/* Force rendering true colors when outputing to pdf */
* {
  -webkit-print-color-adjust: exact;
}

/* Misc */
a.anchor-link {
  display: none;
}

.highlight  {
  margin: 0.4em;
}

/* Input area styling */
.jp-InputArea {
  overflow: hidden;
}

.jp-InputArea-editor {
  overflow: hidden;
}

.CodeMirror pre {
  margin: 0;
  padding: 0;
}

/* Using table instead of flexbox so that we can use break-inside property */
/* CSS rules under this comment should not be required anymore after we move to the JupyterLab 4.0 CSS */


.jp-CodeCell.jp-mod-outputsScrolled .jp-OutputArea-prompt {
  min-width: calc(
    var(--jp-cell-prompt-width) - var(--jp-private-cell-scrolling-output-offset)
  );
}

.jp-OutputArea-child {
  display: table;
  width: 100%;
}

.jp-OutputPrompt {
  display: table-cell;
  vertical-align: top;
  min-width: var(--jp-cell-prompt-width);
}

body[data-format='mobile'] .jp-OutputPrompt {
  display: table-row;
}

.jp-OutputArea-output {
  display: table-cell;
  width: 100%;
}

body[data-format='mobile'] .jp-OutputArea-child .jp-OutputArea-output {
  display: table-row;
}

.jp-OutputArea-output.jp-OutputArea-executeResult {
  width: 100%;
}

/* Hiding the collapser by default */
.jp-Collapser {
  display: none;
}

@media print {
  .jp-Cell-inputWrapper,
  .jp-Cell-outputWrapper {
    display: block;
  }

  .jp-OutputArea-child {
    break-inside: avoid-page;
  }
}
</style>

<!-- Load mathjax -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.7/latest.js?config=TeX-AMS_CHTML-full,Safe"> </script>
    <!-- MathJax configuration -->
    <script type="text/x-mathjax-config">
    init_mathjax = function() {
        if (window.MathJax) {
        // MathJax loaded
            MathJax.Hub.Config({
                TeX: {
                    equationNumbers: {
                    autoNumber: "AMS",
                    useLabelIds: true
                    }
                },
                tex2jax: {
                    inlineMath: [ ['$','$'], ["\\(","\\)"] ],
                    displayMath: [ ['$$','$$'], ["\\[","\\]"] ],
                    processEscapes: true,
                    processEnvironments: true
                },
                displayAlign: 'center',
                CommonHTML: {
                    linebreaks: {
                    automatic: true
                    }
                }
            });

            MathJax.Hub.Queue(["Typeset", MathJax.Hub]);
        }
    }
    init_mathjax();
    </script>
    <!-- End of mathjax configuration --></head>
<body class="jp-Notebook" data-jp-theme-light="true" data-jp-theme-name="JupyterLab Light">

<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h1 id="Regression-Models-for-YouTube-Views-Prediction">Regression Models for YouTube Views Prediction<a class="anchor-link" href="#Regression-Models-for-YouTube-Views-Prediction">&#182;</a></h1><h3 id="Objective:-To-gain-actionable-insights-from-YouTube-data.-We-aim-to-identify-the-most-influential-metrics-and-popular-categories.">Objective: To gain actionable insights from YouTube data. We aim to identify the most influential metrics and popular categories.<a class="anchor-link" href="#Objective:-To-gain-actionable-insights-from-YouTube-data.-We-aim-to-identify-the-most-influential-metrics-and-popular-categories.">&#182;</a></h3><ul>
<li><a href="#Univariate">Univariate Regression</a></li>
<li><a href="#Univariate2">Univariate Regression / No Outliers</a></li>
<li><a href="#Multivariate">Multivariate</a></li>
<li><a href="#Polynomial">Polynomial</a></li>
<li><a href="#Comparison">Comparison, Interpretation and Recommendation</a></li>
</ul>

</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs  ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[1]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Import libraries and set up environment</span>


<span class="kn">import</span> <span class="nn">pandas</span> <span class="k">as</span> <span class="nn">pd</span>
<span class="kn">import</span> <span class="nn">numpy</span> <span class="k">as</span> <span class="nn">np</span>
<span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span>
<span class="c1"># Set Pandas display options to show numbers in a more readable format</span>
<span class="n">pd</span><span class="o">.</span><span class="n">options</span><span class="o">.</span><span class="n">display</span><span class="o">.</span><span class="n">float_format</span> <span class="o">=</span> <span class="s1">'</span><span class="si">{:.2f}</span><span class="s1">'</span><span class="o">.</span><span class="n">format</span>
<span class="kn">from</span> <span class="nn">sklearn.preprocessing</span> <span class="kn">import</span> <span class="n">scale</span><span class="p">,</span> <span class="n">PolynomialFeatures</span>
<span class="kn">from</span> <span class="nn">sklearn.linear_model</span> <span class="kn">import</span> <span class="n">LinearRegression</span>
<span class="kn">from</span> <span class="nn">sklearn.metrics</span> <span class="kn">import</span> <span class="n">mean_squared_error</span><span class="p">,</span> <span class="n">r2_score</span>
<span class="kn">from</span> <span class="nn">sklearn.metrics</span> <span class="kn">import</span> <span class="n">confusion_matrix</span><span class="p">,</span> <span class="n">accuracy_score</span><span class="p">,</span> <span class="n">precision_recall_fscore_support</span><span class="p">,</span> <span class="n">roc_auc_score</span>
<span class="kn">from</span> <span class="nn">sklearn.preprocessing</span> <span class="kn">import</span> <span class="n">LabelEncoder</span>

<span class="o">%</span><span class="k">matplotlib</span> inline
<span class="n">plt</span><span class="o">.</span><span class="n">style</span><span class="o">.</span><span class="n">use</span><span class="p">(</span><span class="s1">'ggplot'</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h2 id="Data-Loading-and-Description">Data Loading and Description<a class="anchor-link" href="#Data-Loading-and-Description">&#182;</a></h2><p>We begin by loading our dataset, which comprises various metrics from YouTube videos, including likes and views, to understand the average interaction metrics and their distributions.</p>
<h2 id="Initial-Analysis">Initial Analysis<a class="anchor-link" href="#Initial-Analysis">&#182;</a></h2><p>We perform an initial analysis to get descriptive statistics, which gives us insights into the mean, standard deviation, and range of views, likes, and other engagement metrics. This analysis will influence our models and preparation.</p>
<ul>
<li>A description of the data is provided here. What it shows is high variance and large numbers. We will see what that reveals, its impact on our model, and potential actions we will take. We will iterate with other models after our Linear Regression</li>
</ul>

</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[2]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Load the provided youtube data and display the first five rows of data.</span>
<span class="n">youtube</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">'CAvideos.csv'</span><span class="p">)</span>

<span class="n">youtube</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
<span class="n">youtube</span><span class="o">.</span><span class="n">describe</span><span class="p">()</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[2]:</div>



<div class="jp-RenderedHTMLCommon jp-RenderedHTML jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/html">
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>category_id</th>
      <th>views</th>
      <th>likes</th>
      <th>dislikes</th>
      <th>comment_count</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>40881.00</td>
      <td>40881.00</td>
      <td>40881.00</td>
      <td>40881.00</td>
      <td>40881.00</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>20.80</td>
      <td>1147035.91</td>
      <td>39582.69</td>
      <td>2009.20</td>
      <td>5042.97</td>
    </tr>
    <tr>
      <th>std</th>
      <td>6.78</td>
      <td>3390913.02</td>
      <td>132689.53</td>
      <td>19008.37</td>
      <td>21579.02</td>
    </tr>
    <tr>
      <th>min</th>
      <td>1.00</td>
      <td>733.00</td>
      <td>0.00</td>
      <td>0.00</td>
      <td>0.00</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>20.00</td>
      <td>143902.00</td>
      <td>2191.00</td>
      <td>99.00</td>
      <td>417.00</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>24.00</td>
      <td>371204.00</td>
      <td>8780.00</td>
      <td>303.00</td>
      <td>1301.00</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>24.00</td>
      <td>963302.00</td>
      <td>28717.00</td>
      <td>950.00</td>
      <td>3713.00</td>
    </tr>
    <tr>
      <th>max</th>
      <td>43.00</td>
      <td>137843120.00</td>
      <td>5053338.00</td>
      <td>1602383.00</td>
      <td>1114800.00</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h2 id="Data-Preparation:">Data Preparation:<a class="anchor-link" href="#Data-Preparation:">&#182;</a></h2><ul>
<li>We use the number of likes as our single predictor variable to fit a linear regression model.</li>
<li>We split our dataset into two halves, one for training and one for testing our model.</li>
<li>We scale the data for better interpretibility since the numbers are very large.</li>
</ul>
<h2 id="Univariate-Regresssion-Model:">Univariate Regresssion Model:<a class="anchor-link" href="#Univariate-Regresssion-Model:">&#182;</a></h2><p><a id='Univariate'></a></p>

</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs  ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[3]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Univariate Regresssion Model</span>
<span class="n">mid</span> <span class="o">=</span> <span class="nb">len</span><span class="p">(</span><span class="n">youtube</span><span class="p">)</span> <span class="o">//</span> <span class="mi">2</span>

<span class="n">X</span> <span class="o">=</span> <span class="n">youtube</span><span class="p">[</span><span class="s1">'likes'</span><span class="p">]</span><span class="o">.</span><span class="n">values</span><span class="p">[:,</span> <span class="n">np</span><span class="o">.</span><span class="n">newaxis</span><span class="p">]</span>
<span class="n">y</span> <span class="o">=</span> <span class="n">youtube</span><span class="p">[</span><span class="s1">'views'</span><span class="p">];</span>
<span class="c1"># scale data down for better readability/interpretability</span>
<span class="n">scaledViews</span> <span class="o">=</span> <span class="n">scale</span><span class="p">(</span><span class="n">y</span><span class="p">)</span>
<span class="n">y</span> <span class="o">=</span> <span class="n">scaledViews</span>
<span class="n">X_train</span> <span class="o">=</span> <span class="n">X</span><span class="p">[</span><span class="mi">0</span><span class="p">:</span><span class="n">mid</span><span class="p">]</span>
<span class="n">X_test</span> <span class="o">=</span> <span class="n">X</span><span class="p">[</span><span class="n">mid</span><span class="p">:]</span>

<span class="n">y_train</span> <span class="o">=</span> <span class="n">y</span><span class="p">[</span><span class="mi">0</span><span class="p">:</span><span class="n">mid</span><span class="p">]</span>
<span class="n">y_test</span> <span class="o">=</span> <span class="n">y</span><span class="p">[</span><span class="n">mid</span><span class="p">:]</span>

<span class="n">linmod</span> <span class="o">=</span> <span class="n">LinearRegression</span><span class="p">()</span>

<span class="n">linmod</span><span class="o">.</span><span class="n">fit</span><span class="p">(</span><span class="n">X_train</span><span class="p">,</span> <span class="n">y_train</span><span class="p">)</span>

<span class="n">preds</span> <span class="o">=</span> <span class="n">linmod</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">X_test</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h2 id="Visualization">Visualization<a class="anchor-link" href="#Visualization">&#182;</a></h2><ul>
<li>We visualize the predicted versus actual values of views using a scatter plot to assess the model fit. We see a clear positive correlation but outliers as well</li>
</ul>

</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[4]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">plt</span><span class="o">.</span><span class="n">scatter</span><span class="p">(</span><span class="n">y_test</span><span class="p">,</span> <span class="n">preds</span><span class="p">,</span><span class="n">color</span><span class="o">=</span><span class="s1">'g'</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s2">"Actual y Value"</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s2">"Predicted y Value"</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s2">"Linear Regression Model"</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>




<div class="jp-RenderedImage jp-OutputArea-output ">
<img src="data:image/png;base64,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"
class="
"
>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h2 id="Model-Evaluation">Model Evaluation<a class="anchor-link" href="#Model-Evaluation">&#182;</a></h2>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[5]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="nb">print</span><span class="p">(</span><span class="n">linmod</span><span class="o">.</span><span class="n">intercept_</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="n">linmod</span><span class="o">.</span><span class="n">coef_</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>


<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain">
<pre>-0.27628730769235516
[6.85656107e-06]
</pre>
</div>
</div>

</div>

</div>

</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<ul>
<li>We calculate the residuals, R-squared, and Mean Squared Error (MSE) on the test set to evaluate model performance.</li>
</ul>

</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[6]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># evaluate</span>
<span class="c1"># Calculate residuals</span>
<span class="n">rss</span> <span class="o">=</span> <span class="nb">sum</span><span class="p">((</span><span class="n">y_test</span> <span class="o">-</span> <span class="n">preds</span><span class="p">)</span> <span class="o">**</span> <span class="mi">2</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="sa">f</span><span class="s2">"RSS = </span><span class="si">{</span><span class="n">rss</span><span class="si">:</span><span class="s2">.3e</span><span class="si">}</span><span class="s2">"</span><span class="p">)</span>

<span class="c1"># Calculate R-squared</span>
<span class="n">rs</span> <span class="o">=</span> <span class="n">r2_score</span><span class="p">(</span><span class="n">y_test</span><span class="p">,</span> <span class="n">preds</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="sa">f</span><span class="s2">"RS = </span><span class="si">{</span><span class="nb">round</span><span class="p">(</span><span class="n">rs</span><span class="p">,</span><span class="w"> </span><span class="mi">3</span><span class="p">)</span><span class="si">}</span><span class="s2">"</span><span class="p">)</span>

<span class="c1"># Calculate MSE</span>
<span class="n">mse</span> <span class="o">=</span> <span class="n">mean_squared_error</span><span class="p">(</span><span class="n">y_test</span><span class="p">,</span> <span class="n">preds</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="sa">f</span><span class="s2">"MSE = </span><span class="si">{</span><span class="nb">round</span><span class="p">(</span><span class="n">mse</span><span class="p">,</span><span class="w"> </span><span class="mi">3</span><span class="p">)</span><span class="si">}</span><span class="s2">"</span><span class="p">)</span>

<span class="c1"># Model with all categories</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>


<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain">
<pre>RSS = 6.384e+03
RS = 0.655
MSE = 0.312
</pre>
</div>
</div>

</div>

</div>

</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h2 id="Interpretation:">Interpretation:<a class="anchor-link" href="#Interpretation:">&#182;</a></h2><p>The R-squared value of 0.65 suggests that 65% of the variance in the views can be explained by the likes. The issue is this doesn't tell the whole story about how the data is affecting video views.</p>
<h3 id="Outliers-and-MSE:">Outliers and MSE:<a class="anchor-link" href="#Outliers-and-MSE:">&#182;</a></h3><p>The presence of outliers, particularly in data like social media views, will skew the data. The median view count is 371,204 vs the mean view count of 1,147,035.91, our intrepretation of this is that we found what are called 'viral' videos, which have extreme view counts.</p>

</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h2 id="Removing-Outliers">Removing Outliers<a class="anchor-link" href="#Removing-Outliers">&#182;</a></h2><ul>
<li>After our initial model we wanted to improve and control for the outliers, when we group the data by category and views,
we find some interesting data. Two categories are massive outliers on youtube, these are Music and Movies. </li>
</ul>

</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[7]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Probably use this bar graph to show more about the data, that some categories are outliers, </span>
<span class="c1"># suggest a user to focus on thos high view categories for success</span>
<span class="c1"># other insights</span>
<span class="c1"># gett the mean views per category</span>
<span class="n">categoryViews</span> <span class="o">=</span> <span class="n">youtube</span><span class="o">.</span><span class="n">groupby</span><span class="p">(</span><span class="s1">'category_id'</span><span class="p">)[</span><span class="s1">'views'</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>
<span class="c1"># sort as desc</span>
<span class="n">categoryViewsSorted</span> <span class="o">=</span> <span class="n">categoryViews</span><span class="o">.</span><span class="n">sort_values</span><span class="p">(</span><span class="n">ascending</span><span class="o">=</span><span class="kc">False</span><span class="p">)</span>
<span class="c1"># bar graph</span>
<span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">(</span><span class="n">figsize</span><span class="o">=</span><span class="p">(</span><span class="mi">15</span><span class="p">,</span> <span class="mi">10</span><span class="p">))</span>
<span class="n">categoryViewsSorted</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">kind</span><span class="o">=</span><span class="s1">'bar'</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s1">'Average Views per Video Category'</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s1">'Video Category'</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s1">'Average Views'</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xticks</span><span class="p">(</span><span class="n">rotation</span><span class="o">=</span><span class="mi">45</span><span class="p">,</span> <span class="n">ha</span><span class="o">=</span><span class="s1">'right'</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">tight_layout</span><span class="p">()</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
<span class="c1"># for reference</span>
<span class="n">categoryMapping</span> <span class="o">=</span> <span class="p">{</span>
    <span class="s2">"1"</span><span class="p">:</span> <span class="s2">"Film &amp; Animation"</span><span class="p">,</span>
    <span class="s2">"2"</span><span class="p">:</span> <span class="s2">"Autos &amp; Vehicles"</span><span class="p">,</span>
    <span class="s2">"10"</span><span class="p">:</span> <span class="s2">"Music"</span><span class="p">,</span>
    <span class="s2">"15"</span><span class="p">:</span> <span class="s2">"Pets &amp; Animals"</span><span class="p">,</span>
    <span class="s2">"17"</span><span class="p">:</span> <span class="s2">"Sports"</span><span class="p">,</span>
    <span class="s2">"18"</span><span class="p">:</span> <span class="s2">"Short Movies"</span><span class="p">,</span>
    <span class="s2">"19"</span><span class="p">:</span> <span class="s2">"Travel &amp; Events"</span><span class="p">,</span>
    <span class="s2">"20"</span><span class="p">:</span> <span class="s2">"Gaming"</span><span class="p">,</span>
    <span class="s2">"21"</span><span class="p">:</span> <span class="s2">"Videoblogging"</span><span class="p">,</span>
    <span class="s2">"22"</span><span class="p">:</span> <span class="s2">"People &amp; Blogs"</span><span class="p">,</span>
    <span class="s2">"23"</span><span class="p">:</span> <span class="s2">"Comedy"</span><span class="p">,</span>
    <span class="s2">"24"</span><span class="p">:</span> <span class="s2">"Entertainment"</span><span class="p">,</span>
    <span class="s2">"25"</span><span class="p">:</span> <span class="s2">"News &amp; Politics"</span><span class="p">,</span>
    <span class="s2">"26"</span><span class="p">:</span> <span class="s2">"Howto &amp; Style"</span><span class="p">,</span>
    <span class="s2">"27"</span><span class="p">:</span> <span class="s2">"Education"</span><span class="p">,</span>
    <span class="s2">"28"</span><span class="p">:</span> <span class="s2">"Science &amp; Technology"</span><span class="p">,</span>
    <span class="s2">"30"</span><span class="p">:</span> <span class="s2">"Movies"</span><span class="p">,</span>
    <span class="s2">"31"</span><span class="p">:</span> <span class="s2">"Anime/Animation"</span><span class="p">,</span>
    <span class="s2">"32"</span><span class="p">:</span> <span class="s2">"Action/Adventure"</span><span class="p">,</span>
    <span class="s2">"33"</span><span class="p">:</span> <span class="s2">"Classics"</span><span class="p">,</span>
    <span class="s2">"34"</span><span class="p">:</span> <span class="s2">"Comedy"</span><span class="p">,</span>
    <span class="s2">"35"</span><span class="p">:</span> <span class="s2">"Documentary"</span><span class="p">,</span>
    <span class="s2">"36"</span><span class="p">:</span> <span class="s2">"Drama"</span><span class="p">,</span>
    <span class="s2">"37"</span><span class="p">:</span> <span class="s2">"Family"</span><span class="p">,</span>
    <span class="s2">"38"</span><span class="p">:</span> <span class="s2">"Foreign"</span><span class="p">,</span>
    <span class="s2">"39"</span><span class="p">:</span> <span class="s2">"Horror"</span><span class="p">,</span>
    <span class="s2">"40"</span><span class="p">:</span> <span class="s2">"Sci-Fi/Fantasy"</span><span class="p">,</span>
    <span class="s2">"41"</span><span class="p">:</span> <span class="s2">"Thriller"</span><span class="p">,</span>
    <span class="s2">"42"</span><span class="p">:</span> <span class="s2">"Shorts"</span><span class="p">,</span>
    <span class="s2">"43"</span><span class="p">:</span> <span class="s2">"Shows"</span><span class="p">,</span>
    <span class="s2">"44"</span><span class="p">:</span> <span class="s2">"Trailers"</span>
<span class="p">}</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>




<div class="jp-RenderedImage jp-OutputArea-output ">
<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAABdEAAAPdCAYAAABlRyFLAAAAOXRFWHRTb2Z0d2FyZQBNYXRwbG90bGliIHZlcnNpb24zLjcuMSwgaHR0cHM6Ly9tYXRwbG90bGliLm9yZy/bCgiHAAAACXBIWXMAAA9hAAAPYQGoP6dpAACMAUlEQVR4nOzdeZiVdd0/8M+BGQREFlkEhNgUdxQ0Q9FENH0yFHEPd3N5FMtKxe33Cyl9TK3UHh/LXAgtTR8Tl8xHVFDpccl9ATVFSFEJEBAUlRn4/v7wmvk5Ml9l9B4PMK/XdXE1597mc7/POV31Pvfcp5RSSgEAAAAAAKykWbkHAAAAAACA1ZUSHQAAAAAAMpToAAAAAACQoUQHAAAAAIAMJToAAAAAAGQo0QEAAAAAIEOJDgAAAAAAGUp0AAAAAADIUKIDAAAAAECGEh0AgCahVCrF0KFDyz0GGQ19fh544IEolUpx7rnnNtpMAAAQoUQHAGhU559/fpRKpSiVSvHyyy+Xe5w13qhRo6JUKsVvfvObz9121113jVKpFH/5y1++gsmI8PzUeP/99+PSSy+NYcOGRZcuXaJFixbRvn372H777eOcc86J11577Usd//e//32USqX4/e9/X8zAAAB8JiU6AEAjSSnFNddcE6VSKSIirr766jJPtOY7/vjjIyLiqquu+sztZsyYEQ8++GBsuOGG8e1vfzsiIl588cW47rrrGn3GpszzE/Hoo4/GJptsEj/60Y/ilVdeib322itOO+20OOqoo6J169Zx8cUXx6abbhpPPfVUuUcFAGAVVZR7AACAtdWkSZNi5syZcdxxx8Xtt98eEyZMiPPPPz9atGhR7tHWWEOHDo3+/fvH008/HU899VQMGjSo3u2uvvrqSCnFMcccE82bN4+IiE033fSrHLVJaurPz4svvhh77rlnvPfee/Hzn/88Tj311KioqPt/uV5//fUYM2ZMLF68uExTAgDQUK5EBwBoJDVX4x577LFx6KGHxrx58+K2226rs82ee+4ZpVIpnn322XqP8Yc//CFKpVKcfvrpdZYvWLAgzjrrrNhss82iVatW0a5du9htt91i0qRJKx3jk7d+uOuuu+Kb3/xmtG3btvYK+YiI2267LQ477LDo379/rLvuutGmTZsYNGhQXHrppbF8+fJ6Z/vHP/4R+++/f3To0CHWXXfd2HHHHeOuu+76zFtNzJ49O04++eTo27dvrLPOOtGxY8fYZ5994vHHH/+sKOs47rjjIiJ/ZX91dXX8/ve/j2bNmsX3vve92uW5e25XV1fHFVdcEYMHD462bdtG69atY+DAgXH55ZfHihUrard77733okWLFrHTTjvV2f/999+PFi1aRKlUiuuvv77OuiuuuCJKpVJce+21tcteffXVOPbYY6Nfv37RsmXL6NChQ2y22WZxwgknxDvvvLNKGdScy1tvvRWHH354dOnSJVq1ahXbbrtt3HDDDdn97rnnnthrr72iU6dOsc4660S/fv3i9NNPj0WLFq20be/evaN3797x7rvvximnnBK9evWKysrKz70HedHPz7/+9a/43ve+FxtssEG0atUqttlmm8+9jUlD3h8RER9++GFccMEFsdVWW0Xr1q2jbdu2sfPOO8ef/vSnz/w9n/b9738/Fi9eHGeccUacccYZKxXoERFf+9rX4k9/+lPssMMOtcuefPLJOOWUU2LrrbeO9ddfP1q2bBkbb7xx/PjHP44FCxbU2X/o0KFx9NFHR0TE0UcfXXu7qFKpFLNmzardblVf1zVSSnHZZZfF5ptvHi1btowNN9wwTj755Hj33XdrXwtfJrdZs2ZFqVSKo446Kl566aU44IADonPnztGsWbN44IEHYvDgwdG8efM65/BJv/jFL6JUKsUvf/nLetcDADSqBABA4ebMmZMqKyvTZpttllJK6bnnnksRkXbbbbc6291www0pItKPf/zjeo/zrW99K0VEev7552uXzZo1K/Xu3TtFRPrmN7+ZfvSjH6XjjjsudevWLZVKpXTllVfWOcb48eNTRKS99torNWvWLA0fPjydfvrp6YADDqjdZpNNNkmbbbZZOuyww9IZZ5yRTjjhhLTRRhuliEjf/e53V5rrxRdfTOuvv36KiPSd73wnnXXWWenggw9OlZWVacSIESki0vjx4+vs8+STT6aOHTumUqmU/u3f/i2deuqp6cgjj0zt2rVLLVq0SHfdddcqZTt37tzUokWL1K5du7R06dKV1k+cODFFRPq3f/u3OssjIu2yyy51li1btiztueeeKSLSpptumk444YR0yimnpAEDBqSISIceemid7YcMGZIqKirSkiVLapfdfffdKSJSRKQjjzyyzvb7779/iog0a9aslFJKb775ZurQoUOqqKhI++yzTxozZkz6wQ9+kPbee+/UunXrOs/zZ4mINGDAgNS7d++09dZbpzFjxqTjjz8+tW/fPkVEuuiii1baZ9y4cSkiUseOHdMRRxyRTjvttLTHHnukiEibb755WrRoUZ3te/Xqlbp27ZoGDRqU+vTpk4477rj0ox/9aKXn9dOKfH7mz5+f+vbtmyIi7bTTTunMM89MRx55ZGrZsmXae++9U0SksWPH1tmnoe+Pjz76KO288861OZx22mnppJNOSp07d04RkcaMGfOZ51vjtddeSxGRWrZsmRYuXLhK+9Q44YQTUpcuXdKBBx6YfvzjH6dTTjklDRkyJEVE2mSTTdLixYtrtx0/fnzte2zEiBFp7Nixtf9qfm9DX9cppXTiiSemiEjdu3dP3//+99Opp56aNt544/T1r389de/ePfXq1etL5TZz5swUEWnIkCGpXbt2afvtt08//OEP07HHHpueeOKJNGHChBQR6eyzz15pthUrVqSNN944rbPOOmnevHkNyhYAoAhKdACARnDBBRekiEg///nPa5cNHDgwlUqlNGPGjNplS5cuTW3btk0bbLBBqqqqqnOM2bNnp2bNmqVBgwbVWb7LLrukUqmUbr755jrLFy5cmLbeeuvUsmXL9Pbbb9curynRS6VSuvvuu+ud99VXX11p2fLly9Ohhx6aIiI98sgjddYNGzYsRUS64oor6iz/61//Wlsof7JsraqqSv369UstW7ZMU6dOrbPPm2++mbp375422GCD9MEHH9Q736cddNBBKSLShAkTVlq31157pYhIt956a53l9ZW0Y8eOTRGRTjnllFRdXV27vLq6Oh1zzDEpItLEiRNrl//f//t/U0TUKfxPO+20VFFRkYYOHZp69OhRu3z58uWpY8eOqW/fvrXLLrvsshQR6ZJLLllp7vfee6/e0rk+NRkfeOCBafny5bXLX3vttdShQ4dUWVlZ53U2efLk2gLz02V5zevjlFNOqbO8V69etR/8vPfee6s0V42inp/jjjsuRUT64Q9/WGf5448/nioqKuot0Rv6/jj//PNTRKThw4fXeQ/OmTMn9ezZM0XESq/Z+tSUwEOGDPncbT9t1qxZdV5/NX7729+miEgXXHBBneU1z1nuA42Gvq4feuihFBGpf//+dT4A+GRR/ukSvaG51ZToEZHOOuuslWb+8MMPU6dOnVLXrl1X+u/C+++/P0VEGjVqVL3nCwDQ2JToAAAFW7FiRerXr19q3rx5evPNN2uX//rXv663QDr22GNTRKS//OUvdZb//Oc/TxGRLrvsstplzzzzTG15Wp/bbrstRUS6/PLLa5fVFG4jRoxo8Lk88cQTKSLSuHHjape9/vrrKSLSRhttVKfArbH77ruvVPDVzHX66afX+3suvfTSejPIue+++1JEpJ133rnO8jfeeCM1b9683iLu0yVtTcndrVu3egvMhQsXplKpVOeK/QceeGClvxwYOHBg2nHHHWsL8pdffjml9PGV9xGRjjvuuNpta14Dn74auqEiIjVv3jy99tprK62rKVDPPffc2mX77rtviog0bdq0eo+3zTbbpM6dO9dZVlOiP/300w2er4jnZ9myZal169ZpvfXWW6n4TymlI488cqUS/Yu8P/r165dKpVLt8/ZJv/vd71JEpKOPPvpzz/nCCy9MEZEOPvjgz912Va1YsSK1bds27brrrnWWf1aJ/kVe19/73veyH3r87W9/q7dEb2huNSX6BhtskD788MN6z/f0009PEZH+/Oc/11le86HMQw89VO9+AACNzReLAgAUbPLkyTFjxoz4t3/7t+jevXvt8lGjRsVpp50W48ePj5/+9Ke190s+6qij4uqrr44JEybEd77zndrtr7/++qisrIxRo0bVLnvkkUciImLRokX13pt63rx5ERHx0ksvrbTuG9/4Rnbmd955Jy6++OL461//Gq+99lq8//77dda/+eabtT8/88wzERGxww47RLNmK3/Fzk477RT33XdfnWU1c8+aNaveuV955ZXauT+ZQc6wYcOiX79+MXXq1Hj55Zdjk002iYiIa6+9NpYvXx5HH310vfej/qR//OMf8c4778TGG28cP/vZz+rdplWrVnWy3GGHHaJVq1YxefLkiPj43tvPPvtsnHPOObHbbrtFRMT9998f/fv3r91m2LBhtfvvs88+cfbZZ8fo0aPj3nvvjW9961sxZMiQ2Hzzzevco35VfO1rX4s+ffqstHzo0KExbty4ePrpp2uXPfLII1FZWRk333xzvcdatmxZzJs3L955553o2LFj7fJ11lkntt566wbNFVHM8/PSSy/F0qVLY+edd4527drVe54TJkyos6yh748lS5bEjBkzokePHtG/f/+Vtt99990jIuKpp576nDP++J7iEdHg5zEioqqqKq688sr405/+FNOnT4933323zn3LP/n++zxf5HVd81r59P3+IyIGDx680nP1ZXLbeuutY5111ql3rn//93+PX/ziF3HllVfGfvvtFxERc+fOjdtuuy0233zz2HnnnevdDwCgsTX5En369Olxxx13xMyZM2PhwoVx2mmnxfbbb9+gY6SU4s4774z7778/5s2bF+3atYtvfetbtf/DDwBoWn73u99FxMfl+Cd17Ngx9t577/jzn/8cd955Z4wcOTIiIoYMGRIbbbRR3HHHHbFw4cLo0KFDPPHEEzFt2rTYd999o1OnTrXHqPniyXvvvTfuvffe7AzvvffeSsu6du1a77aLFi2Kr3/96zFz5szYfvvt44gjjoj1118/KioqYtGiRXHZZZfFRx99VLv9u+++GxERG2ywQb3Hq295zdz//d//nZ05N3d9SqVSHHvssXHWWWfF1VdfHRdffHGsWLEirr322iiVSnW+sDKnZqZXXnklxo0bt0oz1Xyx6H333Rfz58+PBx98MFasWBG77bZbbLHFFtG1a9e4//7748QTT4z7778/SqVSnRK9V69e8fe//z3OPffc+J//+Z+45ZZbIiKiZ8+eMWbMmDj55JNX6fwj8vnXPM81z1PNuVZXV3/medac6ydL9A022OALlcJFPD+f9zqr7/Xc0PdHze/IvTe6detWZ7vPUvOB2ezZsz932087+OCDY+LEidG3b98YMWJEdO3atbZovvTSS+u8/z7PF3ldf1bWzZs3r/Oa+OT2XyS33D4REX379o0999wz7rnnnpg5c2b06dMnxo8fH8uWLYsTTjghux8AQGNb+dKhJuajjz6K3r17xzHHHPOFjzF+/PiYPHlyHH744XHppZfGGWecERtttFGBUwIAa4p58+bFbbfdFhERhxxySJRKpTr//vznP0fE/y/aaxxxxBHx0UcfxU033RQREdddd11ERBx55JF1tqu5Iveyyy6L9PGt+er9N378+JVmy5WhV199dcycOTPGjh0bjz32WFxxxRVx3nnnxbnnnhsHH3zwStu3bds2IiL+9a9/1Xu8+pbXzH377bd/5txjx46t95j1Ofroo6OysjKuu+66qKqqinvvvTf++c9/1l4F/XlqZho5cuRnzjRz5sw6+w0bNixSSjFlypS4//77o1WrVrHDDjvUrpsyZUp89NFHMXXq1Nhiiy2iS5cudfbfbLPN4qabbop33nknnnjiifj5z38eK1asiO9///v1Pm85ufznzJlT5/xqfu7QocNnnmdKKXr16lXnWF+kQK9R1PPzeedZ3z6r+v6o2b6+Y0VEvP3223W2+yw1V3E/8cQTq1S613jiiSdi4sSJsdtuu8VLL70U48ePjwsuuCDOPffc+MlPfhLLli1b5WN9ctaGvK4/6z29fPny2mL+07/ji+T2ea+pk046KVJKcdVVV9X+Z6tWreLwww//zP0AABpTky/RBw4cGIccckj2z5urq6vjD3/4Q5xwwglx+OGHx9lnnx3Tpk2rXT979uy49957Y8yYMbHddttFly5donfv3jFgwICv6hQAgNXIhAkTYtmyZbHtttvG9773vXr/derUKSZNmhT//Oc/a/c74ogjolQqxYQJE6KqqipuvPHG6NSp00q3Nhk8eHBEREydOrWwmV999dWIiNh///1XWvfggw+utGzgwIER8fGtMz55y4kaf/vb31Za1hhzb7DBBrHPPvvE3Llz44477oirr746IiKOP/74Vdp/0003jfbt28ejjz4aVVVVq/x7a27bMnny5Jg8eXLsvPPO0aJFi9p1CxYsiN/85jfx/vvv125bn4qKith2223jjDPOiBtvvDEiIiZOnLjKc7z++usxa9aslZY/8MADEfH/n6eIj/NfuHBhnf8d29iKeH5at24dzzzzTL2ldM15flJDX2frrbde9OvXL958883aWwp90pQpUyIiYtCgQZ97rD59+sTuu+8eH374YVx88cWfu33N1eU1778RI0ZEZWVlnW3+/ve/xwcffLDSvs2bN4+IjwvuT/sir+ua10p9791HH300qqur6ywrMrdP+853vhO9evWKa6+9Nu6+++6YMWNGHHTQQdGhQ4cGHwsAoChNvkT/PFdccUW8/PLL8cMf/jAuvvjiGDx4cPzHf/xH7dUVTz75ZHTp0iWefPLJGD16dIwePTp++9vfrvKfIgMAa5eaovCKK66Iq6++ut5/xx57bKxYsSKuueaa2v169eoVQ4cOjUcffTQuvfTSmD9/fowaNWqlUm277baLnXfeOW699da49tpr653h+eefj7lz567yzL17946I/1981Xj66afjggsuWGn7nj17xtChQ+PVV1+NK6+8ss66//mf/1npfugRHxeE/fr1i//6r/+Kv/71r/XO8cgjj8TSpUtXee6IiOOOOy4iIi6++OK4/fbbo3PnzrHvvvuu0r4VFRXx/e9/P95+++34wQ9+UG9Z+fbbb8f06dPrLNt2222jffv2ceutt8bLL79cpyiv+bkmt0/eyiXi41K0vqt9a5a1bNlylWaP+LhAPeOMM+p8kDFz5sz49a9/HRUVFXHYYYfVLv/Rj34UER/n9dZbb610rPfffz8effTRVf7dq+rLPD+VlZVx6KGHxpIlS1a6v/kTTzwRf/zjH1fa54u8P4455phIKcXpp59ep5SeP39+7T3FV/WvVv/zP/8z2rZtGxdccEH88pe/XKl8jvj4w49DDjmk9v7tNe+/T38oMHfu3Bg9enS9v6fm9ipvvPHGSuu+yOv6iCOOiIiI888/v84HFsuWLYuzzz673hmKzO2TmjVrFieccEL861//imOPPTYiPr5XOgBAWRX9TaVrsgMPPDA99thjtY/ffvvtdNBBB6V33nmnznY//elP0x//+MeUUkpXXnllGjVqVDr77LPT9OnT0wsvvJBOP/30dO65536lswMA5TdlypQUEWmrrbb6zO1effXVVCqV0oYbbpiqq6trl//+979PEZEqKytTRKQnn3yy3v3feOONtPHGG6eISFtvvXU6/vjj05gxY9KoUaPSlltumSIiPfLII7Xbjx8/PkVEGj9+fL3He/PNN9P666+fmjVrlkaOHJnGjBmTRo4cmSorK9PBBx+cIiIdeeSRdfaZNm1aat++fYqINHz48HT22WenQw45JFVWVqYRI0akiEgTJkyos8+zzz6bunbtmiIi7bjjjumkk05Kp512Wjr44INT3759U0Skt99++zOz+7QVK1akPn36pIhIEZFOO+207LYRkXbZZZc6y5YtW5b22WefFBFpww03TIcffng688wz0zHHHJN23nnn1KxZs3TBBResdKyac4yI9MQTT9RZ169fvxQRqXnz5mnRokV11p1yyimpoqIi7bbbbumEE05IZ555ZjrwwANTy5Yt0zrrrJP+9re/rdJ5R0QaMGBA6t27d9pmm23SmDFj0gknnFD7nFx00UUr7fPzn/88lUql1Lp163TAAQek008/PZ144olpr732Suuuu27ac88962zfq1ev1KtXr1WaJ+fLPj/z5s2rfW3stNNO6cwzz0xHHnlkatmyZe3zNnbs2Dr7NPT98dFHH6WddtopRUTaYost0umnn55Gjx6dunTpkiIijRkzpkHn/Mgjj6Tu3buniEg9e/ZMRx11VDr77LPTKaeckoYOHZoqKytTixYt0lNPPZVSSqm6ujoNGTIkRUTaYYcd0umnn56OOOKI1Llz57TTTjul7t27r/Q8LFiwILVu3Tq1a9cunXzyyelnP/tZ+tnPflb7evsir+vjjz++dvsf/OAH6dRTT039+/dPX//611P37t1Tnz596mzf0NxmzpxZ73+X1Odf//pXatGiRe3rHACg3JTon/DpEv3hhx9OBx54YDrssMPq/DvkkEPSr371q5RSSr/97W/TgQcemN58883a/WbMmLHSMgBg7Tdq1KgUEemyyy773G133XXXFBHpjjvuqF22ZMmStO6666aISFtuueVn7r948eJ0/vnnp0GDBqV11103tWzZMvXu3Tvttdde6corr0zvvfde7bafV6Kn9HEpvvfee6fOnTun1q1bp0GDBqWrrrrqM4uvF198MY0cOTK1a9cutW7dOg0ePDj95S9/SRdffHGKiHTbbbettM+//vWvdMYZZ6QtttgitWrVKq277rppo402Svvvv3+6/vrrU1VV1edm92nnnXdebUn70ksvZberr6RN6eOi97rrrkvDhg1LHTp0SJWVlal79+5pyJAh6fzzz0+vv/76Svv8+te/ThGROnTokJYvX15nXU0Zuf3226+036OPPpr+/d//PQ0YMCB16NAhtWzZMvXr1y8dddRR6fnnn1/lc645lzfffDMdeuihqXPnzmmdddZJAwcOrL3Yoz5Tp05NBx54YOrWrVuqrKxMnTp1SltvvXX60Y9+lB5//PE62xZRoqf05Z+ft99+Ox199NGpU6dOqWXLlmnrrbdO48ePr/3Q6tMlekoNe3+klNIHH3yQzj///LTFFlukli1bpjZt2qQhQ4akG2644Qud85IlS9KvfvWrNHTo0NS5c+dUUVGR2rZtmwYNGpTOPPPM9Nprr9XZ/p133kknnnhi6tWrV1pnnXVS375901lnnZXef//97PNw9913p8GDB9f+d0ZEpJkzZ9aub+jrevny5elXv/pV2mSTTVKLFi1St27d0kknnZQWLVqU2rRpk7bZZpuVZmhIbg0p0VNKaeTIkSki0hVXXLFK2wMANKZSSikVdln7Gu6ggw6K0047LbbffvuIiHj44Yfj17/+dfzqV7+KZs3q3vmmZcuW0b59+7j55ptj4sSJtfexjPj4zx4PO+yw+D//5/+4NzoA0OQceuihccMNN8RLL70Um2yySbnHWSuVSqXYZZdd6r0vOBTplVdeif79+8chhxxS5//zNKYVK1ZEv379Yt68efHWW2/VfvEpAEC5uCf6Z+jdu3esWLEi3n333ejatWudf+3bt4+IiE022SSWL19e55vpa+4z2alTp3KMDQDQ6FasWFHnf//UuP/+++Omm26KLbbYQoEOa5A5c+as9EXBS5cujR/+8IcRUf8XDzeWm2++OWbNmhVHHHGEAh0AWC1UlHuAcvvwww/r/B/AuXPnxqxZs6JNmzbRvXv32GmnneLyyy+PI444Ivr06ROLFy+OF154Ib72ta/FoEGDYquttoo+ffrEb37zmzjqqKMipRTXXHNNDBgwILp3717GMwMAaDzLli2Lnj17xq677hqbbrppVFRUxLRp0+Lee++NddZZJ6644opyjwg0wKWXXho33nhjDB06NLp16xZz5syJ+++/P2bPnh3f+c53vpIS/bzzzosFCxbENddcE23atImzzjqr0X8nAMCqaPK3c5k2bVqMGzdupeW77LJLjB49Oqqrq+PWW2+NBx98MBYsWBDrrbde9O/fPw466KD42te+FhERCxYsiGuvvTaee+65WGeddWLgwIFxxBFHRJs2bb7q0wEA+EosX748fvzjH8eUKVPijTfeiPfeey86deoU3/zmN+Pss8+OrbfeutwjrtXczoWi3X///XHJJZfEM888E/Pnz4/mzZvHJptsEqNGjYpTTjklKisrG32GUqkUlZWVscUWW8Qvf/nLGDZsWKP/TgCAVdHkS3QAAAAAAMhxT3QAAAAAAMhQogMAAAAAQIYSHQAAAAAAMirKPUA5LVy4MKqrq8s9xmfq3LlzzJs3r9xjrBVkWSx5FkeWxZJncWRZHFkWS57FkWWx5FkcWRZHlsWSZ3FkWSx5FkeWxVkTsqyoqIgOHTp8/nZfwSyrrerq6qiqqir3GFmlUikiPp7T979+ObIsljyLI8tiybM4siyOLIslz+LIsljyLI4siyPLYsmzOLIsljyLI8virG1Zup0LAAAAAABkKNEBAAAAACBDiQ4AAAAAABlKdAAAAAAAyFCiAwAAAABAhhIdAAAAAAAylOgAAAAA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Md55552GHrLWNddcE6+//nr89Kc//dxtP/2nADVPRn1/IlBZWRmVlZX1Hmd1fhIbS1M858bS1LNMKTX5DIoiy2LJsziyLI4siyXP4siyWPIsjiyLI8tiybM4siyWPIsjy+KsLVk2a+gOH3zwQbadr66uXqlYX1XXXnttPPnkkzF27Njo2LHjZ25bcxuZT1q8eHE0b978M28DAwAAAAAADdHgEr1Lly7xj3/8o951r776anTv3r1Bx0spxTXXXBOPPfZY/OQnP4kuXbp87j4bb7xxPPfcc3WWPfvss9G3b9+V7ocOAAAAAABfVINL9J122iluv/32ePzxx+vcQuXVV1+Nu+++O3beeecGHe+aa66JqVOnximnnBKtWrWKRYsWxaJFi2LZsmW129xwww1x+eWX1z7eY489Yv78+TFhwoSYPXt2TJ48OSZPnhx77713Q08HAAAAAACyGnzZ9ogRI+Lll1+OX/ziF7HuuutGRMT5558fS5YsiW222Sb22muvBh1v0qRJERFx7rnn1ll+0kknxdChQyMiYuHChTF//vzadV26dImzzjorJkyYEPfcc0906NAhjj766Bg8eHBDTwcAAAAAALIaXKJXVFTEWWedFQ8//HA89dRT8e6778Z6660X2267bey4447RrFnDLm6/+eabP3eb0aNHr7Rs8803jwsvvLBBvwsAAAAAABriC91AvFQqxZAhQ2LIkCFFzwMAAAAAAKuNBt8THQAAAAAAmopVuhJ93Lhxceyxx8aGG24Y48aN+8xtS6VS/OQnPylkOAAAAAAAKKcGX4meUvpS6wEAAAAAYE2xSleijx07tvbnc889t7FmAQAAAACA1coqXYl+0UUXxZNPPhkrVqxo7HkAAAAAAGC1sUpXoj/33HPx5JNPRvv27WOXXXaJoUOHRvfu3Rt7NgAAAAAAKKtVKtGvuuqq+N///d+YMmVK3H777XH77bfHpptuGrvuumvssMMOsc466zT2nAAAAAAA8JVbpRK9VatWsfvuu8fuu+8eb775ZkyZMiWmTp0av/nNb2L8+PExZMiQ2HXXXWPjjTdu7HkBAAAAAOArs0ol+idtuOGGcdhhh8WoUaPiqaeeigceeCAeeOCBuP/++2PDDTeMYcOGxfDhwxtjVgAAAAAA+Eo1uESv0axZs9huu+1iu+22i8WLF8ftt98ef/nLX+L6669XogMAAAAAsFb4wiV6RMTy5cvjiSeeiClTpsSzzz4bERG9e/cuYi4AAAAAACi7L1Siv/766zF58uT429/+FkuWLIl11103vvWtb8WwYcOU6AAAAAAArDVWuURfunRpTJ06NR544IF47bXXIiJiyy23jF133TW+8Y1vRGVlZaMNCQAAAAAA5bBKJfpll10Wjz/+eFRVVcX6668f++23X+y6667RpUuXxp4PAAAAAADKZpVK9Mceeyy22267GDZsWGy99dZRKpUaey4AAAAAACi7VSrRf/vb30bbtm0bexYAAAAAAFitNFuVjRToAAAAAAA0RatUogMAAAAAQFOkRAcAAAAAgAwlOgAAAAAAZCjRAQAAAAAgo+KL7vjmm2/G9OnTY8mSJTFs2LBo3759LFiwINq0aRMtWrQockYAAAAAACiLBpfoK1asiCuvvDIeeOCB2mXbbLNNtG/fPn73u99Fnz594uCDDy5yRgAAAAAAKIsG387l1ltvjb/97W9x+OGHxy9/+cs66wYOHBjPPPNMUbMBAAAAAEBZNfhK9AceeCD233//GD58eKxYsaLOui5dusTcuXMLGw4AAAAAAMqpwVeiL1iwIPr371/vusrKyvjwww+/9FAAAAAAALA6aHCJ3q5du+zV5m+99Vasv/76X3ooAAAAAABYHTS4RB84cGDceuutsWDBgtplpVIpli5dGnfffXdsu+22hQ4IAAAAAADl0uB7oh900EHx9NNPx49+9KPYYostIiLixhtvjDfeeCOaN28eBxxwQOFDAgAAAABAOTT4SvT27dvHBRdcEEOGDImZM2dGs2bN4p///Gdss802cd5550WbNm0aY04AAAAAAPjKNfhK9IiPi/Tjjz++6FkAAAAAAGC10uAr0QEAAAAAoKlo8JXoV1xxRXZds2bNonXr1rHRRhvF9ttvHxUVX+hCdwAAAAAAWC00uOWeNm1aLF26NJYuXRrNmjWL9dZbL5YsWRIrVqyI1q1bR0TEXXfdFd27d4+xY8dG+/bti54ZAAAAAAC+Eg0u0U899dT4xS9+Eccdd1wMHjw4mjVrFitWrIhHHnkk/vjHP8aPf/zjWL58efziF7+IG2+8MU488cTGmBsAAAAAABpdg++Jft1118Xee+8dO+64YzRr9vHuzZo1iyFDhsTw4cNjwoQJsckmm8SIESPimWeeKXpeAAAAAAD4yjS4RJ8xY0b06NGj3nU9e/aMWbNmRURE7969Y8mSJV9qOAAAAAAAKKcGl+itWrWKadOm1bvuhRdeiFatWkVExLJly2p/BgAAAACANVGD74m+0047xe233x4ppdhhhx2iXbt28e6778bDDz8cd955Z+y1114REfHaa6/FhhtuWPjAAAAAAADwVWlwiT5q1KhYuHBh3HbbbXHbbbfVWTdkyJD47ne/GxER/fv3j2222aaIGQEAAAAAoCwaXKJXVFTEKaecEvvvv39Mnz493nvvvWjTpk1svvnmde6VPmDAgEIHBQAAAACAr1qDS/QaPXr0yH7BKAAAAAAArA2+cIkeEbF48eJYtmzZSss7der0ZQ4LAAAAAACrhS9Uov/5z3+Ou+++O5YsWVLv+ptuuulLDQUAAAAAAKuDZg3dYfLkyXHbbbfFt7/97YiIGDlyZIwcOTI6duwY3bp1i3//938vfEgAAAAAACiHBpfo99xzT21xHhGx/fbbxyGHHBKXXnpptGrVKnt1OgAAAAAArGkaXKLPmTMn+vfvH6VSKSIiqqurIyKiRYsWMXz48LjvvvuKnRAAAAAAAMqkwSV68+bNIyKiVCpFq1atYsGCBbXr1ltvvTqPAQAAAABgTdbgEr1bt24xf/78iIjo169f3H///VFdXR0rVqyI++67Lzp37lz4kAAAAAAAUA4NLtG32WabePHFFyPi4y8VfeGFF+Loo4+Oo48+Oh577LEYMWJE4UMCAAAAAEA5VDR0hwMPPLD25y233DJ+9rOfxcMPPxwREYMGDYott9yyuOkAAAAAAKCMGlSiL1u2LB566KHYdNNNo0ePHhERsdFGG8VGG23UKMMBAAAAAEA5Neh2Li1atIjx48fH4sWLG2seAAAAAABYbTT4nuhdunSJRYsWNcIoAAAAAACwemlwib7XXnvFbbfdFkuXLm2MeQAAAAAAYLXR4C8WfeONN2LJkiUxevTo2HLLLaNDhw511pdKpTj66KMLGxAAAAAAAMqlwSX6PffcU/vz3//+93q3UaIDAAAAALA2aHCJftNNNzXGHAAAAAAAsNpp8D3RAQAAAACgqWjwleg1nnnmmZg+fXosXrw4DjjggOjUqVO8+uqr0aVLl2jbtm2RMwIAAAAAQFk0uET/6KOP4qKLLooXXnihdtkee+wRnTp1ijvvvDM6duwYRxxxRKFDAgAAAABAOTT4di433nhjvPbaa3HqqafGhAkT6qzbeuut4/nnny9sOAAAAAAAKKcGX4n+6KOPxsEHHxzbb799rFixos66Tp06xfz58wsbDgAAAAAAyqnBV6IvXrw4evToUe+6UqkUy5Yt+9JDAQAAAADA6qDBJfr6668fr7/+er3r/vnPf0aXLl2+9FAAAAAAALA6aHCJvv3228fEiRNj5syZtctKpVLMmzcv7rrrrthhhx0KHRAAAAAAAMqlwfdEP/DAA+OFF16Is88+O3r27BkREVdccUX861//iu7du8e+++5b9IwAAAAAAFAWDS7RW7VqFeedd1789a9/jaeeeiq6du0a66yzTuy7777xne98J1q0aNEYcwIAAAAAwFeuwSV6RESLFi1i3333ddU5AAAAAABrtQbfE/26666L2bNnN8YsAAAAAACwWmnwlej33HNP3HXXXdG3b98YNmxYDBkyJFq3bt0YswEAAAAAQFk1+Er0q666Kr73ve9Fs2bN4uqrr47jjz8+fv3rX8fzzz/fGPMBAAAAAEDZNPhK9NatW8cee+wRe+yxR8yePTseeOCBmDp1avzv//5vdOzYMYYOHRoHHXRQY8wKAAAAAABfqQZfif5JPXr0iMMOOyx+85vfxOmnnx4ppfjzn/9c1GwAAAAAAFBWDb4S/dPeeuuteOCBB+Khhx6KhQsXRseOHYuYCwAAAAAAyu4LlegffvhhPPzwwzFlypT4xz/+ERUVFfH1r389hg0bFltttVXRMwIAAAAAQFk0uES//PLL47HHHotly5ZF375943vf+14MGTIk1l133caYDwAAAAAAyqbBJfqzzz4b3/rWt2Lo0KHxta99baX1ixcvjrZt2xYyHAAAAAAAlFODS/Tf/va30bx58zrLUkrx9NNPx+TJk+Opp56KG264obABAQAAAACgXBpcon+yQJ8zZ05MmTIlHnzwwVi4cGFUVFTEN77xjUIHBAAAAACAcmlwib5s2bJ49NFHY/LkyfHiiy/WLh8+fHjsu+++sd566xU6IAAAAAAAlMsql+ivvvpqTJ48OR5++OH44IMPomXLljF06ND4xje+ERdeeGFsu+22CnQAAAAAANYqq1Sin3baafHGG29ERET//v1j1113jR133DFatmwZS5cubdQBAQAAAACgXFapRK8p0AcNGhSHHnpo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IiLipvkexEz06yQ9PV3/+Mc/dOzYMbm5uWn58uWaM2eOli1bJomrilVBLc2Tk5Ojt99+W7169dL48eM1a9YstW/fXikpKZo9e7aOHz/u6ibWKMePH9cLL7ygefPm6auvvuIny1chNzdXM2bM0D333KOxY8fq5Zdflr+/v1JTU13dtBrJEaD37dtXAwYM0Lp165w/aUTVubu765ZbblG7du104MABLVq0SD///LMkfiJaFRkZGXrppZcUFxen8ePH61//+peKi4u1e/duVzetRjp//rzeffddde3aVYmJiZo9e7Z69uypAwcO6MMPP2RMr4Jjx47ppZdeUvv27fXMM8/olVdeUUFBgd5//31JfM6ras2aNWrTpo0SEhJUq1Yt/fDDD0pJSdGePXt0+vRpVzevRnEEa/fcc4/uvfdeVzenRmMMMld6eromTJig0NBQDRw4UJ07d9bMmTOVmprKMbOKHJ/z/v3768knn9Qtt9yiffv2qbS01NVNq3HS09P1/PPPa/DgwUpISJDdbldWVpYOHDigkpISVzevxnHU8/jx4/Ly8tKXX36pmTNnatWqVZJujiyOmejXQUlJiRYvXqyYmBj95S9/kXThZ2OLFi3Sxo0bVVRU5LyqeDNcubka1NJcmZmZcnNzU9euXeXl5SVJGjhwoHbs2KFTp07piy++0KhRo+Tr6+villZ/BQUFWrRoke68805FRkZq9uzZstlsGjRokPz9/V3dvBonJydHRUVF6tixo/O2evXq6fjx43rllVcUGRmpLl26qFGjRi5sZc1w8OBBJSUlqX///ho5cqQ2b96sNWvW6Pjx4woICJDNZpPVyjX1ynKMLd7e3rr11lv1pz/9SZMnT9aXX34pPz8/ffPNN+revTt98woKCgq0cOFCderUSUOHDpXFYpHFYlFUVJSys7P18ccfq02bNmrSpAnH0ErKz8/X2bNn1bp1a+e4/cADD6hevXpau3atkpOT9cc//pFfSV1BYWGhFi5cqA4dOmj48OHO42PPnj21detWF7euZjpy5IjatGkjSZowYYKkC+fvtWrVUlBQkMaMGcMxsxKOHTum559/XgMHDtSIESNUUlKiH3/8UdnZ2fL391fLli1Vp04dVzezRmAMMte5c+c0Z84cdenSRaNGjZIkdenSRYcOHdK6des0ZswYvptX0okTJzR+/HgNGTJE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uHCh9u/fr06dOrm6OTWOYy9hdktHdUPfNBdjkHnom+ahluainuahluahlua63HjOhnhV06xZMz3yyCPOzYEdfbVjx47OMB1wBY6b5qGW5mIMKouZ6NeYY3Onjz76SHv37tWrr756Uyy2f61899132rt3r7Zs2aIXXniBDV9+B8fVWHd3d61Zs0Y+Pj568cUXnUvlAK5C3zQfY5A56JvmoZbmop7moZbmoZbmYzw3h7u7u7p16+bsoyzbguqC46Z5qKX5GIN+w0z06yQsLExTp05VkyZNXN2UGq1x48bKzc1VUlLSTXnVy0xt27aVJE2aNElRUVEubg3wG/qm+RiDzEHfNA+1NBf1NA+1NA+1NB/j+dVzBGxAdcRx0zzU0nyMQZLF7vitA66pi9dlwtUpKSlhYyeTXLzTN1Cd0DfNxRhkHvqmeailuaineaileailuRjPgRsfx03zUEtzMQYRogMAAAAAAAAAYIjfMgEAAAAAAAAAYIAQHQAAAAAAAAAAA4ToAAAAAAAAAAAYIEQHAAAAAAAAAMAAIToAAAAAAAAAAAYI0QEAAAAAAAAAMODu6gYAAAAArjJt2jTt3LlT77//vmrXrl3hY95++219++23evfdd7Vz507NnDlTM2bMUEhIyGVfe+LEiWX+fb39/PPP+uqrr7R//37l5ubK09NTYWFhiouLU1xcnLy9vav0eps2bdKZM2fUv3//a9RiAAAAoHoiRAcAAMBNq0ePHvrhhx+0adMm9enTp9z9eXl52rp1q9q3b6+AgAC1b99ekyZNUmBgoAtaW3nJyclasGCBmjdvruHDh6tBgwYqLCzU/v37NX/+fGVkZGj06NFVes1NmzbpyJEjhOgAAAC46RCiAwAA4KbVrl07BQYGat26dRWG6Js2bVJRUZF69OghSfL395e/v//1bmaVfPvtt1qwYIF69OihRx55RBaLxXlfu3btFB8fr19++cWFLby2SkpKZLFY5Obm5uqmAAAA4AZBiA4AAICbltVqVdeuXbV48WKlpaUpPDy8zP3r169XYGCg2rVr5/zzpcu52O12paSkaOXKlTpz5oxCQ0M1YsSICv++vLw8LViwQN9//72ys7Pl7++vTp06acSIEWWWVykqKtKCBQu0efNm5+M6dOigkSNHGi4747BgwQLVrl1bY8aMKROgO/j4+Kht27bOP69YsULffvutjh49qsLCQoWEhCguLk79+/eXu/uFrwsTJ07Uvn37JEnDhg1zPjc5OVnSheB6yZIl2rhxozIzM+Xj46M77rhDCQkJZS46FBcX69NPP9XGjRuVn5+vqKgojRo1Sq+//rpatGihxx9/3PnYtLQ0ffbZZ/r5559VVFSkRo0aqX///urWrZvzMXv37lVSUpKeeOIJpaamavPmzcrJydE///lPjRs3TsOHD9eQIUPKvP99+/Zp4sSJGjt2rDp16nTZWgIAAAASIToAAABucj169NCSJUu0du3aMkucpKen68CBAxo8eLCsVqvh8+fPn++c+R0TE6OsrCzNmjVLNptNjRo1cj6usLBQEydO1KlTpzRkyBA1adJER44cUXJystLS0pSYmCiLxSK73a5p06Zpz549Gjx4sKKjo3X48GElJyfr119/1aRJk+Th4VFhW06fPq0jR44oNjZWXl5elXr/J06cUOfOnRUSEiJ3d3cdPnxYCxcu1NGjR/XYY49Jkh566CHNmjVLJ06c0LPPPlvm+TabTa+++qp+/vlnxcfHq1mzZsrKylJycrImTpyoV155RZ6enpKkmTNnasuWLYqPj1erVq2Unp6uadOmKT8/v8xrZmRkKDExUf7+/hozZox8fX21ceNGzZw5U2fOnFF8fHyZx3/yySdq1qyZHn74YVmtVtWpU0d33nmnVq9erfj4+DL//1asWKHAwEB17NixUvUBAAAACNEBAABwU2vQoIGio6O1ceNGJSQkOGdfr127VpLUvXt3w+eeP39eS5YsUceOHfWXv/zFeXtYWJgSExPLhOhfffWVDh8+rMmTJysqKkqS1Lp1awUFBemf//yndu7cqXbt2mnXrl3atWuXEhISNGjQIElSmzZtVLduXb355pv65ptv1KtXrwrbk5WVJUlX3PT0YqNGjXL+t81mU3R0tPz8/DRz5kz9x3/8h3x9fRUaGqratWvLw8NDzZo1K/P8b7/9Vjt37tS4ceN01113OW9v0qSJ/v73v2v9+vXq3bu30tPTtXnzZsXHx+vBBx90vq86derorbfeKvOaycnJKikp0YQJExQcHCxJat++vXMm/z333KNatWo5H1+/fn0988wzZV7j3nvvVVJSkrZt2+YMzLOzs/XDDz/o/vvvZ7kXAAAAVJrxlBoAAADgJtGjRw+dPXtW27ZtkySVlpZq48aN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"
class="
"
>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h2 id="Univariate-without-outliers">Univariate without outliers<a class="anchor-link" href="#Univariate-without-outliers">&#182;</a></h2><p><a id='Univariate2'></a></p>

</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[8]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># SECOND Univariate Regresssion Model</span>

<span class="c1"># ##############################</span>
<span class="c1"># Filter out outlier category_id 10 and 30</span>
<span class="n">filteredIndices</span> <span class="o">=</span> <span class="p">(</span><span class="n">youtube</span><span class="p">[</span><span class="s1">'category_id'</span><span class="p">]</span> <span class="o">!=</span> <span class="mi">10</span><span class="p">)</span> <span class="o">&amp;</span> <span class="p">(</span><span class="n">youtube</span><span class="p">[</span><span class="s1">'category_id'</span><span class="p">]</span> <span class="o">!=</span> <span class="mi">30</span><span class="p">)</span>
<span class="n">filteredData</span> <span class="o">=</span> <span class="n">youtube</span><span class="p">[</span><span class="n">filteredIndices</span><span class="p">]</span>

<span class="c1"># Update X and y variables</span>
<span class="n">X</span> <span class="o">=</span> <span class="n">filteredData</span><span class="p">[</span><span class="s1">'likes'</span><span class="p">]</span><span class="o">.</span><span class="n">values</span><span class="p">[:,</span> <span class="n">np</span><span class="o">.</span><span class="n">newaxis</span><span class="p">]</span>
<span class="n">y</span> <span class="o">=</span> <span class="n">filteredData</span><span class="p">[</span><span class="s1">'views'</span><span class="p">]</span>
<span class="c1"># ##############################</span>
<span class="n">scaledViews</span> <span class="o">=</span> <span class="n">scale</span><span class="p">(</span><span class="n">y</span><span class="p">)</span>
<span class="n">y</span> <span class="o">=</span> <span class="n">scaledViews</span>
<span class="n">mid</span> <span class="o">=</span> <span class="nb">len</span><span class="p">(</span><span class="n">youtube</span><span class="p">)</span> <span class="o">//</span> <span class="mi">2</span>
<span class="n">X_train</span> <span class="o">=</span> <span class="n">X</span><span class="p">[</span><span class="mi">0</span><span class="p">:</span><span class="n">mid</span><span class="p">]</span>
<span class="n">X_test</span> <span class="o">=</span> <span class="n">X</span><span class="p">[</span><span class="n">mid</span><span class="p">:]</span>
<span class="n">y_train</span> <span class="o">=</span> <span class="n">y</span><span class="p">[</span><span class="mi">0</span><span class="p">:</span><span class="n">mid</span><span class="p">]</span>
<span class="n">y_test</span> <span class="o">=</span> <span class="n">y</span><span class="p">[</span><span class="n">mid</span><span class="p">:]</span>
<span class="n">linmod</span> <span class="o">=</span> <span class="n">LinearRegression</span><span class="p">()</span>
<span class="n">linmod</span><span class="o">.</span><span class="n">fit</span><span class="p">(</span><span class="n">X_train</span><span class="p">,</span> <span class="n">y_train</span><span class="p">)</span>
<span class="n">preds</span> <span class="o">=</span> <span class="n">linmod</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">X_test</span><span class="p">)</span>
<span class="c1"># evaluate</span>
<span class="n">rss1</span> <span class="o">=</span> <span class="nb">sum</span><span class="p">((</span><span class="n">y_test</span> <span class="o">-</span> <span class="n">preds</span><span class="p">)</span> <span class="o">**</span> <span class="mi">2</span><span class="p">)</span>
<span class="n">rs1</span> <span class="o">=</span> <span class="n">r2_score</span><span class="p">(</span><span class="n">y_test</span><span class="p">,</span> <span class="n">preds</span><span class="p">)</span>
<span class="n">mse1</span> <span class="o">=</span> <span class="n">mean_squared_error</span><span class="p">(</span><span class="n">y_test</span><span class="p">,</span> <span class="n">preds</span><span class="p">)</span>

<span class="c1"># Display the results</span>
<span class="nb">print</span><span class="p">(</span><span class="sa">f</span><span class="s2">"RSS: </span><span class="si">{</span><span class="n">rss</span><span class="si">:</span><span class="s2">.3e</span><span class="si">}</span><span class="s2"> vs</span><span class="si">{</span><span class="n">rss1</span><span class="si">:</span><span class="s2"> .3e</span><span class="si">}</span><span class="s2">. A </span><span class="si">{</span><span class="p">((</span><span class="n">rss</span><span class="w"> </span><span class="o">-</span><span class="w"> </span><span class="n">rss1</span><span class="p">)</span><span class="w"> </span><span class="o">/</span><span class="w"> </span><span class="n">rss</span><span class="w"> </span><span class="o">*</span><span class="w"> </span><span class="mi">100</span><span class="p">)</span><span class="si">:</span><span class="s2">.2f</span><span class="si">}</span><span class="s2">% improvement."</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="sa">f</span><span class="s2">"MSE: </span><span class="si">{</span><span class="nb">round</span><span class="p">(</span><span class="n">mse</span><span class="p">,</span><span class="w"> </span><span class="mi">3</span><span class="p">)</span><span class="si">}</span><span class="s2"> vs </span><span class="si">{</span><span class="nb">round</span><span class="p">(</span><span class="n">mse1</span><span class="p">,</span><span class="w"> </span><span class="mi">3</span><span class="p">)</span><span class="si">}</span><span class="s2">. A </span><span class="si">{</span><span class="p">((</span><span class="n">mse</span><span class="w"> </span><span class="o">-</span><span class="w"> </span><span class="n">mse1</span><span class="p">)</span><span class="w"> </span><span class="o">/</span><span class="w"> </span><span class="n">mse</span><span class="w"> </span><span class="o">*</span><span class="w"> </span><span class="mi">100</span><span class="p">)</span><span class="si">:</span><span class="s2">.2f</span><span class="si">}</span><span class="s2">% improvement."</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="sa">f</span><span class="s2">"RS2: </span><span class="si">{</span><span class="nb">round</span><span class="p">(</span><span class="n">rs1</span><span class="p">,</span><span class="w"> </span><span class="mi">3</span><span class="p">)</span><span class="si">}</span><span class="s2"> vs </span><span class="si">{</span><span class="nb">round</span><span class="p">(</span><span class="n">rs</span><span class="p">,</span><span class="w"> </span><span class="mi">3</span><span class="p">)</span><span class="si">}</span><span class="s2">. Similar values"</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>


<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain">
<pre>RSS: 6.384e+03 vs 4.204e+03. A 34.15% improvement.
MSE: 0.312 vs 0.252. A 19.41% improvement.
RS2: 0.636 vs 0.655. Similar values
</pre>
</div>
</div>

</div>

</div>

</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h2 id="What-We-Found">What We Found<a class="anchor-link" href="#What-We-Found">&#182;</a></h2><ul>
<li>Its clear the second model that controls for outliers performs much better to predict the impact of youtube 'likes' on its 'view' count.</li>
<li>If you want success on Youtube, the data says to put your content in Music/Movie categories, and maximize the 'likes' engagement metric. </li>
</ul>

</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">

</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs  ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[&nbsp;]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span>
</pre></div>

     </div>
</div>
</div>
</div>

</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h2 id="Next-Steps---Polynomial-Model-and-Interaction-Terms">Next Steps - Polynomial Model and Interaction Terms<a class="anchor-link" href="#Next-Steps---Polynomial-Model-and-Interaction-Terms">&#182;</a></h2><p><a id='Polynomial'></a></p>
<ul>
<li>The last model we will use is another Linear Regression but with interaction terms and polynomial etc etc</li>
</ul>

</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[9]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Select featuress and target variable for the model</span>
<span class="n">X</span> <span class="o">=</span> <span class="n">youtube</span><span class="p">[[</span><span class="s1">'likes'</span><span class="p">,</span> <span class="s1">'comment_count'</span><span class="p">,</span> <span class="s1">'dislikes'</span><span class="p">]]</span>
<span class="n">y</span> <span class="o">=</span> <span class="n">youtube</span><span class="p">[</span><span class="s1">'views'</span><span class="p">]</span>

<span class="c1"># adding teh interaction terms</span>
<span class="n">poly</span> <span class="o">=</span> <span class="n">PolynomialFeatures</span><span class="p">(</span><span class="mi">2</span><span class="p">,</span> <span class="n">interaction_only</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">polyX</span> <span class="o">=</span> <span class="n">poly</span><span class="o">.</span><span class="n">fit_transform</span><span class="p">(</span><span class="n">X</span><span class="p">)</span>
<span class="c1"># SCALE IT</span>
<span class="n">scaledViews</span> <span class="o">=</span> <span class="n">scale</span><span class="p">(</span><span class="n">y</span><span class="p">)</span>
<span class="n">y</span> <span class="o">=</span> <span class="n">scaledViews</span>
<span class="c1"># DEFINE TRAIN/TEST SETS</span>
<span class="n">X_train</span> <span class="o">=</span> <span class="n">polyX</span><span class="p">[</span><span class="mi">0</span><span class="p">:</span><span class="n">mid</span><span class="p">]</span>
<span class="n">X_test</span> <span class="o">=</span> <span class="n">polyX</span><span class="p">[</span><span class="n">mid</span><span class="p">:]</span>

<span class="n">y_train</span> <span class="o">=</span> <span class="n">y</span><span class="p">[</span><span class="mi">0</span><span class="p">:</span><span class="n">mid</span><span class="p">]</span>
<span class="n">y_test</span> <span class="o">=</span> <span class="n">y</span><span class="p">[</span><span class="n">mid</span><span class="p">:]</span>

<span class="c1"># FIT THE MODEL</span>
<span class="n">linmod3</span> <span class="o">=</span> <span class="n">LinearRegression</span><span class="p">()</span>

<span class="n">linmod3</span><span class="o">.</span><span class="n">fit</span><span class="p">(</span><span class="n">X_train</span><span class="p">,</span> <span class="n">y_train</span><span class="p">)</span>

<span class="c1"># DO PREDICTION</span>
<span class="n">preds3</span> <span class="o">=</span> <span class="n">linmod3</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">X_test</span><span class="p">)</span>

<span class="n">plt</span><span class="o">.</span><span class="n">scatter</span><span class="p">(</span><span class="n">y_test</span><span class="p">,</span> <span class="n">preds3</span><span class="p">,</span><span class="n">color</span><span class="o">=</span><span class="s1">'g'</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s2">"Actual y Value"</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s2">"Predicted y Value"</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>

<span class="c1"># MSE and RS function</span>
<span class="n">mse3</span> <span class="o">=</span> <span class="n">mean_squared_error</span><span class="p">(</span><span class="n">y_test</span><span class="p">,</span> <span class="n">preds3</span><span class="p">)</span>
<span class="n">rs3</span> <span class="o">=</span> <span class="n">r2_score</span><span class="p">(</span><span class="n">y_test</span><span class="p">,</span> <span class="n">preds3</span><span class="p">)</span>
<span class="n">rss3</span> <span class="o">=</span> <span class="nb">sum</span><span class="p">((</span><span class="n">y_test</span> <span class="o">-</span> <span class="n">preds3</span><span class="p">)</span> <span class="o">**</span> <span class="mi">2</span><span class="p">)</span>
<span class="c1"># Print it</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">"RSS:"</span><span class="p">,</span> <span class="n">rss3</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="s1">'Mean Squared Error:'</span><span class="p">,</span><span class="nb">round</span><span class="p">(</span><span class="n">mse3</span><span class="p">,</span> <span class="mi">3</span><span class="p">))</span>
<span class="nb">print</span><span class="p">(</span><span class="s1">'R Squared:'</span><span class="p">,</span><span class="nb">round</span><span class="p">(</span><span class="n">rs3</span><span class="p">,</span> <span class="mi">3</span><span class="p">))</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>




<div class="jp-RenderedImage jp-OutputArea-output ">
<img src="data:image/png;base64,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9913Y82aNXaPMZvNuPfee/HAAw9IPm9FRQUWLVqEiooKJZpJRC5igkM0SJSWlgIAfvrpJ1RVVbl0jqamJmzbts1jCY47abVa/PKXv0RVVRVqampsHvPvf/8bP//8M6ZPn+7h1hHRQDHBIRoEfvjhB5w6dQoTJkwAAOzdu9fLLfINlsTFXjxKS0utiRAR+RfuJk40CFge4Lfffjva29tx4MAB3HnnnQgKCup13Pnz57F161Z89dVXaG5uxpAhQ5Camoply5bhzJkz1g0sX3jhBbzwwgsAgIULF2LRokXWoaS+Q0obN25EZWUlNm7caH1t69at+PLLL1FXVwez2YyYmBjMmjUL06ZNgyAIsr63f/7zn/j888/x4osv9vt+1q1bh5aWFjz11FM2PxsfH4/U1FR8+umnWLJkCQICAqzvtbe348iRI8jIyEB4eDh++OEHFBcXo6qqCs3NzYiMjERKSgqWLFmC6Ohoh22UExuTyYQdO3bg008/RUNDA0JCQjBx4kTccccdGDJkiIzIEA1uTHCIVK67uxufffYZxowZg8TEREybNg0vvvgiDh48aN0lGriU3KxevRomkwkLFixAUlIS2tra8PXXX6O9vR2jRo3CihUr8MILL+DXv/61tTdo2LBhstvU2NiI//qv/7LuqFxVVYWXX34Z58+fx8KFC2Wda/bs2SgtLUVZWRlmzJhhfb2mpgYVFRVYtmyZw89Pnz4dL774Io4ePYprr73W+npZWRmMRqO1l6exsRFxcXHIysqCXq9Hc3MzSkpKsHr1ajz11FOKJB9msxn5+fn47rvvMH/+fKSmpuLcuXPYsmULHnnkETz++OMIDAwc8HWIBgMmOEQqd+jQIXR0dFgf1FlZWSgoKEBpaWmvBOedd95Ba2srnnjiCcTHx1tfz8rKsv47ISEBABATE4PU1FSX27RixQrrv81mM9LT0yGKIj744APccsstsnpxkpKSkJaWht27d/dKcD788EOEhIRgypQpDj/fMx49E5zS0lIMGzYMV199NQDguuuuw3XXXder3RMmTMDdd9+NsrIyzJ49W3Kb7Tl48CC++uor3H///cjMzOz1Pa5evRqffPIJsrOzB3wdosGACQ6Ryu3duxeBgYG44YYbAADBwcG47rrr8Mknn6Curg6xsbEAgK+++gpXXXVVr+TGXb799lsUFhaiuroaFy5c6PVeS0sLIiMjZZ1v9uzZ+Mc//oHvv/8eV1xxBTo6OrB//35MnToVwcHBDj8bHByM66+/Hvv377cOPZ0+fRonTpzALbfcAo3mUqliZ2cntm3bhsOHD6OxsRFms9l6jjNnzshqrz1ffPEFwsLCMHHiRFy8eNH6+uWXX47IyEhUVFQwwSGSiAkOkYrV19fju+++Q2ZmJkRRRHt7OwBYE5zS0lLcfvvtAIDW1lYMHTrU7W2qrq7G+vXrkZ6ejnvuuQfDhg2DVqvFkSNHsH37dnR3d8s+Z0ZGBqKjo7F7925cccUV+OSTT9DV1YWbbrpJ0uenT5+O0tJS7N+/H/PmzUNpaSkEQcC0adOsxzzzzDP49ttvccstt2DMmDEICQmBIAh47LHHXGqzLS0tLWhvb7f+TPpqa2tT5DpEgwETHCIV27t3L0RRxKFDh3Do0KF+7+/btw+33XYbNBoNhgwZgvPnz7t8LZ1Oh46Ojn6v930of/bZZwgICEBOTk6vepIjR464fG2NRoNZs2Zh8+bN+N3vfoeSkhJcddVViIuLk/T5sWPHYuTIkfjkk08we/ZsfPrpp7jqqqswYsQIAEBHRweOHj2KhQsX4uabb7Z+zmg0wmAwOD2/1NiEh4cjPDwc/+f//B+b5wkJCZH0/RARExwi1TKbzdi3bx8uu+wy/OEPf+j3/hdffIGdO3fiyy+/xMSJE3HNNddg//79qK2ttZsY6HQ6ALDZYxEdHY1Dhw7BaDRaj2tra8OxY8cQGhpqPU4QBAQEBFiHfizn279//4C+3xkzZmDr1q149tlnUVtbiyVLlsj6/LRp0/DGG2/g7bffRmtra6/eGwAQRdH6fVns2bOn11CVPVJjM3HiRBw4cABmsxkpKSmy2k9EvTHBIVKpL7/8Ek1NTViyZAnS09P7vZ+QkIDdu3dj7969mDhxIm699VZ89dVXePjhh7FgwQIkJiaivb0dX331FebMmYORI0fisssuQ2BgID799FOMHDkSwcHBiIqKwtChQ3HjjTfi448/xnPPPYcZM2agra0NRUVFvR7gADBhwgTs3LkTzz77LP7rv/4LbW1tKC4u7pc8yBUWFoYpU6agpKQE0dHRmDhxoqzPT5kyBZs3b0ZxcTHCwsIwadIk63uhoaG48sorUVRUhPDwcERHR6OyshKlpaUICwtzem6psbnhhhtQVlaGxx57DLNnz0ZycjICAgLw888/o6KiAtdee22vdhGRfVzoj0il9u7dC61W268nwmLIkCG49tprcfToUTQ3N2Po0KH4+9//jgkTJuC9997Dhg0b8PLLL6OjowN6vR4AEBQUhHvvvRcGgwHr16/H6tWr8fHHHwMArrjiCqxcuRI//fQT8vPzsX37dtx8881IS0vrdd2rrroK9957L06fPo28vDy8/fbbuO666zB//vwBf8+WGV8zZ87s1UMkRUREBCZOnAhRFHHDDTf0m479pz/9Cenp6XjjjTfw5JNP4sSJE3jooYf6JSm2SI2NRqPBqlWrsGDBAhw+fBhPPPEEnnjiCezYsQM6nQ6JiYmyvieiwUwQRVH0diOIiJTw2muvoaSkBP/85z8RHh7u7eYQkRdxiIqI/N7x48dRV1eH3bt3Y+bMmUxuiIg9OETk/xYtWoSgoCCMHz8eK1ascLr2DRGpHxMcIiIiUh0WGRMREZHqMMEhIiIi1WGCQ0RERKrDBIeIiIhUhwkOERERqQ4THCIiIlIdJjhERESkOkxwiIiISHX+P/X0kvHz3dqtAAAAAElFTkSuQmCC"
class="
"
>
</div>

</div>

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>


<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain">
<pre>RSS: 5417.034573487704
Mean Squared Error: 0.265
R Squared: 0.707
</pre>
</div>
</div>

</div>

</div>

</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h3 id="Interpretation-of-Polynomial-Model">Interpretation of Polynomial Model<a class="anchor-link" href="#Interpretation-of-Polynomial-Model">&#182;</a></h3><ul>
<li>Here is what we found and our suggestions from this model etc etc</li>
</ul>

</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs  ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[&nbsp;]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

     </div>
</div>
</div>
</div>

</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h2 id="Next-Steps---Multivariate-Model">Next Steps - Multivariate Model<a class="anchor-link" href="#Next-Steps---Multivariate-Model">&#182;</a></h2><p><a id='Multivariate'></a>
To try to capture more complexity and improve predictions, we'll proceed with a multivariate model that includes additional predictors. This will also help us understand the combined effect of multiple engagement metrics on video views and hopefully lead to a better model.</p>

</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[10]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Import necessary libraries</span>
<span class="kn">import</span> <span class="nn">pandas</span> <span class="k">as</span> <span class="nn">pd</span>
<span class="kn">import</span> <span class="nn">numpy</span> <span class="k">as</span> <span class="nn">np</span>
<span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span>
<span class="kn">from</span> <span class="nn">sklearn.preprocessing</span> <span class="kn">import</span> <span class="n">scale</span>
<span class="kn">from</span> <span class="nn">sklearn.linear_model</span> <span class="kn">import</span> <span class="n">LinearRegression</span>
<span class="kn">from</span> <span class="nn">sklearn.metrics</span> <span class="kn">import</span> <span class="n">mean_squared_error</span><span class="p">,</span> <span class="n">r2_score</span>

<span class="c1"># Load dataset</span>
<span class="n">youtube</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s1">'CAvideos.csv'</span><span class="p">)</span>

<span class="c1"># Define predictor variables and response variable</span>
<span class="n">X</span> <span class="o">=</span> <span class="n">youtube</span><span class="p">[[</span><span class="s1">'likes'</span><span class="p">,</span> <span class="s1">'dislikes'</span><span class="p">,</span> <span class="s1">'comment_count'</span><span class="p">]]</span>
<span class="n">y</span> <span class="o">=</span> <span class="n">youtube</span><span class="p">[</span><span class="s1">'views'</span><span class="p">]</span>

<span class="c1"># Split the dataset into training and testing sets</span>
<span class="n">mid</span> <span class="o">=</span> <span class="nb">len</span><span class="p">(</span><span class="n">youtube</span><span class="p">)</span> <span class="o">//</span> <span class="mi">2</span>
<span class="n">scaledViews</span> <span class="o">=</span> <span class="n">scale</span><span class="p">(</span><span class="n">y</span><span class="p">)</span>
<span class="n">y</span> <span class="o">=</span> <span class="n">scaledViews</span>
<span class="n">X_train</span> <span class="o">=</span> <span class="n">X</span><span class="o">.</span><span class="n">iloc</span><span class="p">[:</span><span class="n">mid</span><span class="p">]</span>
<span class="n">X_test</span> <span class="o">=</span> <span class="n">X</span><span class="o">.</span><span class="n">iloc</span><span class="p">[</span><span class="n">mid</span><span class="p">:]</span>
<span class="n">y_train</span> <span class="o">=</span> <span class="n">y</span><span class="p">[:</span><span class="n">mid</span><span class="p">]</span> 
<span class="n">y_test</span> <span class="o">=</span> <span class="n">y</span><span class="p">[</span><span class="n">mid</span><span class="p">:]</span>  

<span class="c1"># Create the linear regression model</span>
<span class="n">linmod2</span> <span class="o">=</span> <span class="n">LinearRegression</span><span class="p">()</span>

<span class="c1"># Fit the model on the training data</span>
<span class="n">linmod2</span><span class="o">.</span><span class="n">fit</span><span class="p">(</span><span class="n">X_train</span><span class="p">,</span> <span class="n">y_train</span><span class="p">)</span>

<span class="c1"># Make predictions on the test data</span>
<span class="n">preds2</span> <span class="o">=</span> <span class="n">linmod2</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">X_test</span><span class="p">)</span>

<span class="c1"># Visualize tghe relationship between actual and predicted values</span>
<span class="n">plt</span><span class="o">.</span><span class="n">scatter</span><span class="p">(</span><span class="n">y_test</span><span class="p">,</span> <span class="n">preds2</span><span class="p">,</span> <span class="n">color</span><span class="o">=</span><span class="s1">'blue'</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s2">"Actual Views"</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s2">"Predicted Views"</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s2">"Multivariate Linear Regression Model"</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>

<span class="c1"># Output the model's intercept and coefficients</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">"Intercept:"</span><span class="p">,</span> <span class="n">linmod2</span><span class="o">.</span><span class="n">intercept_</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">"Coefficients:"</span><span class="p">,</span> <span class="n">linmod2</span><span class="o">.</span><span class="n">coef_</span><span class="p">)</span>

<span class="c1"># Evaluate the model</span>
<span class="n">rss2</span> <span class="o">=</span> <span class="nb">sum</span><span class="p">((</span><span class="n">y_test</span> <span class="o">-</span> <span class="n">preds2</span><span class="p">)</span> <span class="o">**</span> <span class="mi">2</span><span class="p">)</span>
<span class="n">rsq2</span> <span class="o">=</span> <span class="n">r2_score</span><span class="p">(</span><span class="n">y_test</span><span class="p">,</span> <span class="n">preds2</span><span class="p">)</span>
<span class="n">mse2</span> <span class="o">=</span> <span class="n">mean_squared_error</span><span class="p">(</span><span class="n">y_test</span><span class="p">,</span> <span class="n">preds2</span><span class="p">)</span>

<span class="nb">print</span><span class="p">(</span><span class="s2">"RSS:"</span><span class="p">,</span> <span class="nb">round</span><span class="p">(</span><span class="n">rss2</span><span class="p">,</span> <span class="mi">3</span><span class="p">))</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">"R-squared:"</span><span class="p">,</span> <span class="nb">round</span><span class="p">(</span><span class="n">rsq2</span><span class="p">,</span> <span class="mi">3</span><span class="p">))</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">"MSE:"</span><span class="p">,</span> <span class="nb">round</span><span class="p">(</span><span class="n">mse2</span><span class="p">,</span> <span class="mi">3</span><span class="p">))</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>




<div class="jp-RenderedImage jp-OutputArea-output ">
<img src="data:image/png;base64,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naiWGOAQ1TE//PADbt26haeffhodO3Y0uz8pKQmbNm3C1q1b0a1bNzz55JM4evQoZs2ahREjRiA5ORklJSU4evQohgwZgsaNG6NBgwYIDg7Grl270LhxY4SGhiImJgb169fHww8/jM2bN+PDDz9E//79UVxcjDVr1pgENwBw3333Yd26dfjggw/wyCOPoLi4GGvXrjUGRbXRr18/bNq0CevXr0fjxo3Rtm1bu4/p2bMndu/ejTfffBODBw9Gq1atEBQUhBs3buDHH3/E7373O9x///0A9Cu2DKNDCQkJSExMBAC0bdvWmGD86KOPmjz//PnzkZycjBYtWiAyMhIFBQVYv3494uPjjY8nIucxwCGqY7Zu3QqlUml1FCMyMhK/+93vcODAARQWFqJ+/fr4xz/+gRUrVuCbb75BcXExIiMj0a5dO2OF4JCQELz00ktYtWoV5s6di6qqKmMdnHbt2mHKlCn45ptvsGDBAjRo0ACjR4/GDz/8gJMnTxpf95577sFLL72E1atXIyMjA/Xr10f//v0RGRmJjz76qFbvuXnz5mjevDnOnTvn0OgNoA9apk6dig0bNmDnzp3IyspCUFAQYmNj0b59eyQnJ5scf++99+Lw4cMmicQqlQrt2rVDTk6Oye2G93vgwAFs2bIFZWVliI6ORqdOnTBq1CgolfzVTFRbkhBCeLsRRERERK7EZeJEREQUcBjgEBERUcBhgENEREQBhwEOERERBRwGOERERBRwGOAQERFRwGGAQ0RERAGHAQ4REREFHAY4REREFHAY4BAREVHAYYBDREREAYcBDhEREQWc/w+jUNU+HLyOVwAAAABJRU5ErkJggg=="
class="
"
>
</div>

</div>

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>


<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain">
<pre>Intercept: -0.2543667977302746
Coefficients: [ 7.02530954e-06  1.47410331e-05 -1.21136758e-05]
RSS: 5192.256
R-squared: 0.719
MSE: 0.254
</pre>
</div>
</div>

</div>

</div>

</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h2 id="Interpretations-of-Multivariate-Model">Interpretations of Multivariate Model<a class="anchor-link" href="#Interpretations-of-Multivariate-Model">&#182;</a></h2><ul>
<li>Its clear this model performs much better than the single predictor model with 'likes' only, the addition of other engagement metrics like comment count and dislikes captures much more. This model also outperformed the Polynomial and Interaction model with the same features, suggesting x y z</li>
</ul>

</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h2 id="Which-was-the-best-model?-A-comparison">Which was the best model? A comparison<a class="anchor-link" href="#Which-was-the-best-model?-A-comparison">&#182;</a></h2><p><a id='Comparison'></a></p>

</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs  ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[11]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Gather all the evaluation metrics for each model we did.</span>

<span class="c1"># print(f"\nUnivariate Model - \n  RSS: {round(rss, 3)}, \n  R-Squared: {round(rs, 3)}, \n  MSE: {round(mse, 3)}")</span>
<span class="c1"># print(f"\nUnivariate Model/No Outliers - \n  RSS: {round(rss1, 3)}, \n  RS: {round(rs1, 3)}, \n  MSE: {round(mse1, 3)}")</span>
<span class="c1"># print(f"\nMultivariate Model - \n  RSS: {round(rss2, 3)}, \n  R-squared: {round(rsq2, 3)}, \n  MSE: {round(mse2, 3)}")</span>
<span class="c1"># print(f"\nPolynomial, Interaction Term Model - \n  RSS: {round(rss3, 3)}, \n  R-Squared: {round(rs3, 3)}, \n  MSE: {round(mse3, 3)}")</span>
</pre></div>

     </div>
</div>
</div>
</div>

</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h2 id="Comparisons-and-Recommendations">Comparisons and Recommendations<a class="anchor-link" href="#Comparisons-and-Recommendations">&#182;</a></h2>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p><strong>Univariate Model:</strong></p>
<ul>
<li>RSS: 6384.342</li>
<li>R-Squared: 0.655</li>
<li>MSE: 0.312<ul>
<li>Good R-squared value but higher MSE compared to others.</li>
</ul>
</li>
</ul>
<p><strong>Univariate Model/No Outliers:</strong></p>
<ul>
<li>RSS: 4204.271 (↓34.15% from Univariate Model)</li>
<li>RS: 0.636 (↓2.90% from Univariate Model)</li>
<li>MSE: 0.252 (↓19.23% from Univariate Model)<ul>
<li>Improvement in both RSS and MSE compared to the first model, but slightly lower R-squared.</li>
</ul>
</li>
</ul>
<p><strong>Multivariate Model:</strong></p>
<ul>
<li>RSS: 5192.256 (↑23.50% from Univariate Model/No Outliers)</li>
<li>R-squared: 0.719 (↑13.11% from Univariate Model/No Outliers)</li>
<li>MSE: 0.254 (↑0.79% from Univariate Model/No Outliers)<ul>
<li>Best R-squared value and comparable MSE to the no-outliers model, this indicates it explains variance in the data well while maintaining accuracy.</li>
</ul>
</li>
</ul>
<p><strong>Polynomial, Interaction Term Model:</strong></p>
<ul>
<li>RSS: 5417.035 (↑4.33% from Multivariate Model)</li>
<li>R-Squared: 0.707 (↓1.67% from Multivariate Model)</li>
<li>MSE: 0.265 (↑4.33% from Multivariate Model)<ul>
<li>Similar R-squared to the multivariate model but higher MSE.</li>
</ul>
</li>
</ul>
<p><hr>
Comparing the R-squared and MSE of the multivariate model with the other models, it is very clear that the multivariate model is better for predictions of view counts. After conducting these models, the recommendation remains the same: for success on YouTube, focus on content in categories like Music and Movies and optimize engagement metrics such as likes above all else, while also paying attention to comments and minimizing dislikes.</p>
<h3 id="Winner?">Winner?<a class="anchor-link" href="#Winner?">&#182;</a></h3><p>Multivariate Regression Model with [ likes, dislikes, comments ] as predictors</p>

</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs  ">
<div class="jp-Cell-inputWrapper">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[&nbsp;]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span> 
</pre></div>

     </div>
</div>
</div>
</div>

</div>
</body>







</html>
