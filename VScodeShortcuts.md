

1.
Go to Definition
Select a symbol then type F12. Alternatively, you can use the context menu or Ctrl+click (Cmd+click on macOS).
You can go back to your previous location with the Go > Back command or Ctrl+Alt+-.
You can also see the type definition if you press Ctrl (Cmd on macOS) when you are hovering over the type.

2. 
Peek References
Select a symbol then type Shift+F12. Alternatively, you can use the context menu.

Find All References view
Select a symbol then type Shift+Alt+F12 to open the References view showing all your file's symbols in a dedicated view.'

3. 

CTRL+SHIFT+[
To fold(hide) the code

CTRL+SHIFT+]
To unfold(show) the code

4.
Alt+Down
To move the current selected line one line down

Alt+Up
To move the currently selected line one line up

5. Navigation history
Navigate entire history: Ctrl+Tab

Navigate back: Ctrl+Alt+-

Navigate forward: Ctrl+Shift+-

6. navigating working files in Visual Studio Code

Ctrl + Tab
Ctrl + Shift + Tab

7. Switch between consecutive tabs

ctrl + pg up/pg dn

8. Code Folding
Fold All: Ctrl + k + 0 (zero)
Unfold All:  Ctrl + k + j

Ctrl + K + 0: fold all levels (namespace, class, method, and block)
Ctrl + K + 1: namspace
Ctrl + K + 2: class
Ctrl + K + 3: methods
Ctrl + K + 4: blocks
Ctrl + K + [ or Ctrl + k + ]: current cursor block
Ctrl + K + j: UnFold

9. console.log(object)

clg Tab

10. TS/JS posfix completion


Template		Outcome
.if				if (expr)
.else			if (!expr)
.null			if (expr === null)
.notnull		if (expr !== null)
.undefined		if (expr === undefined)
.notundefined	if (expr !== undefined)
.for			for (let i = 0; i < expr.Length; i++)
.forof			for (let item of expr)
.foreach		expr.forEach(item => )
.not			!expr
.return			return expr
.var			var name = expr
.let			let name = expr
.const			const name = expr
.log			console.log(expr)
.error			console.error(expr)
.warn			console.warn(expr)
.cast			(<SomeType>expr)
.castas			(expr as SomeType)

11. Turbo console log extension

Insert -> Alt + S
Delete -> Alt + Shift + S
Comment -> Alt + Shift + C
Uncomment -> Alt + Shift + /                  																												/

12. Prettier 

Ctrl + K Ctrl + F -> Format selected text

13. Move line Up/Down

Alt + Up/Down Arrow

14. Indent line

ctrl + ]

15. Navigation history

Navigate entire history: Ctrl+Tab
Navigate back: Ctrl+Alt+-   -> ctrl + Q
Navigate forward: Ctrl+Shift+- -> ctrl+shift+Q

16. Toggle Fold 
(Ctrl+K Ctrl+L)


<!--!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!-->
<!--      _____ _    _  _____ _______ ____  __  __     -->
<!--     / ____| |  | |/ ____|__   __/ __ \|  \/  |    -->
<!--    | |    | |  | | (___    | | | |  | | \  / |    -->
<!--    | |    | |  | |\___ \   | | | |  | | |\/| |    -->
<!--    | |____| |__| |____) |  | | | |__| | |  | |    -->
<!--     \_____|\____/|_____/   |_|  \____/|_|  |_|    -->
<!--                                                   -->
<!--                                                   -->
<!--!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!-->

1. Toggle Minimap
	Ctrl+M Ctrl+M

2. Copy path
	alt+x

	copy relative path
	alt+shift+x

3. Toggle quotes

	ctrl + '                                                                                                                                                   '

https://dev.to/selrond/tips-to-use-vscode-more-efficiently-3h6p

4. Quick open files for real

	"workbench.editor.enablePreviewFromQuickOpen": false

5. Hide Open Editors section

	  "explorer.openEditors.visible": 0

6. Minimap

	"editor.minimap.renderCharacters": false,
	"editor.minimap.maxColumn": 200,
	"editor.minimap.showSlider": "always"

7. Smooth scrolling

	"editor.smoothScrolling": true

8. Caret improvements

	"editor.cursorBlinking": "phase"
	"editor.cursorSmoothCaretAnimation": true

9. Telemetry

	"workbench.settings.enableNaturalLanguageSearch": false
	"telemetry.enableCrashReporter": false
	"telemetry.enableTelemetry": false,

9.   Bold function names

	"editor.tokenColorCustomizations": {
	    "textMateRules": [
	      {
	        "scope": [
	          "entity.name.function",
	          "support.function"
	        ],
	        "settings": {
	          "fontStyle": "bold"
	        }
	      }
	    ]
	  }

10. Italics

	"editor.tokenColorCustomizations": {
	  "textMateRules": [
	    {
	      "scope": [
	        //following will be in italic (=FlottFlott)
	        "comment",
	        "entity.name.type.class", //class names
	        "keyword", //import, export, return…
	        "constant", //String, Number, Boolean…, this, super
	        "storage.modifier", //static keyword
	        "storage.type.class.js", //class keyword
	      ],
	      "settings": {
	        "fontStyle": "italic"
	      }
	    },
	    {
	      "scope": [
	        //following will be excluded from italics (VSCode has some defaults for italics)
	        "invalid",
	        "keyword.operator",
	        "constant.numeric.css",
	        "keyword.other.unit.px.css",
	        "constant.numeric.decimal.js",
	        "constant.numeric.json"
	      ],
	      "settings": {
	        "fontStyle": ""
	      }
	    }
	  ]
	}

11. Jump to Closing tag in VS Code

	Shift + Q
	Ctrl + Shift + \

12. Search input in Search view
Find input in Find widget

alt+up : Shows the previous term in history
alt+down : Shows the next term in history
Customize key board short cuts

search.history.showPrevious : alt+up
search.history.showNext : alt+down
find.history.showPrevious : alt+up
find.history.showNext : alt+down

13. Copy line up/down
Ctrl+Alt+up/down arrow

14. workbench.action.toggleEditorWidths
Ctrl+Alt+E

15. go back / back

Ctrl + Q

16. Overview ruler
This ruler is located beneath the scroll bar on the right edge of the editor and gives an overview of the decorations in the editor.

editorOverviewRuler.border: Color of the overview ruler border.
editorOverviewRuler.findMatchForeground: Overview ruler marker color for find matches. The color must not be opaque to not hide underlying decorations.
editorOverviewRuler.rangeHighlightForeground: Overview ruler marker color for highlighted ranges, like by the Quick Open, Symbol in File and Find features. The color must not be opaque to not hide underlying decorations.
editorOverviewRuler.selectionHighlightForeground: Overview ruler marker color for selection highlights. The color must not be opaque to not hide underlying decorations.
editorOverviewRuler.wordHighlightForeground: Overview ruler marker color for symbol highlights. The color must not be opaque to not hide underlying decorations.
editorOverviewRuler.wordHighlightStrongForeground: Overview ruler marker color for write-access symbol highlights. The color must not be opaque to not hide underlying decorations.
editorOverviewRuler.modifiedForeground: Overview ruler marker color for modified content.
editorOverviewRuler.addedForeground: Overview ruler marker color for added content.
editorOverviewRuler.deletedForeground: Overview ruler marker color for deleted content.
editorOverviewRuler.errorForeground: Overview ruler marker color for errors.
editorOverviewRuler.warningForeground: Overview ruler marker color for warnings.
editorOverviewRuler.infoForeground: Overview ruler marker color for infos.
editorOverviewRuler.bracketMatchForeground: Overview ruler marker color for matching brackets.




=====================================================================================================
  ____ _______ _    _ ______ _____    ______ _____ _____ _______ ____  _____   _____
 / __ \__   __| |  | |  ____|  __ \  |  ____|  __ \_   _|__   __/ __ \|  __ \ / ____|
| |  | | | |  | |__| | |__  | |__) | | |__  | |  | || |    | | | |  | | |__) | (___
| |  | | | |  |  __  |  __| |  _  /  |  __| | |  | || |    | | | |  | |  _  / \___ \
| |__| | | |  | |  | | |____| | \ \  | |____| |__| || |_   | | | |__| | | \ \ ____) |
 \____/  |_|  |_|  |_|______|_|  \_\ |______|_____/_____|  |_|  \____/|_|  \_\_____/

================================================================================================

/**********************************************************/
/*      _____ _    _ ____  _      _____ __  __ ______     */
/*     / ____| |  | |  _ \| |    |_   _|  \/  |  ____|    */
/*    | (___ | |  | | |_) | |      | | | \  / | |__       */
/*     \___ \| |  | |  _ <| |      | | | |\/| |  __|      */
/*     ____) | |__| | |_) | |____ _| |_| |  | | |____     */
/*    |_____/ \____/|____/|______|_____|_|  |_|______|    */
/*                                                        */
/*                                                        */
/**********************************************************/

1. Pretty JSON
Ctrl + Alt + J
	
2. Highlightwords user settings

{
	// The colors to highlight texts are specified by a list of theme scope names,
	// and HighlightWords uses this list in circular order.
	"colors_by_scope": [
		"string",
		"entity.name.class",
		"variable.parameter",
		"invalid.deprecated",
		"invalid",
		"support.function"
	],
	"whole_word": false,
	"use_regex": false,
	"ignore_case": true,

	// Keywords to be always highlighted, clear the list to disable it.
	// "keyword" are literally matched, and "color" refers to theme scope names.
	// "flag": 0 - regex, 1 - literal (default), 2 - regex and ignore case, 3 - literal and ignore case
	// Note that json has some special characters like '\' should be escaped.
	"permanent_highlight_keyword_color_mappings": [
		{"keyword": "(?<=CST)(?s).*?(?=CSP)", "color": "entity.name.class", "flag" : 2},
		// {"keyword": "(?<=CST)(.*)(?=CSP)", "color": "entity.name.class", "flag" : 2},
		{"keyword": "TODO", "color": "invalid.deprecated", "flag" : 3},
		{"keyword": "CST", "color": "variable.parameter", "flag" : 3},
		{"keyword": "CSP", "color": "variable.parameter", "flag" : 3},
		{"keyword": "console.log(", "color": "invalid", "flag" : 3},
		{"keyword": "// console.log(", "color": "string", "flag" : 3},
		{"keyword": "FIXIT .*", "color": "support.function", "flag": 2},
	]

}

3. Cycle between search results 
In the find panel, Enter and Shift + Enter will cycle forward and backward between matches.


EXTENSIONS NOT WORKING.

1. JS BOOSTER
2. TURBO CONSOLE log
3. LEAPER
4. QUOKKA.JS
