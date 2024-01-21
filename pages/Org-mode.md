# Shortcut keys
- Jumping between headers
	- There are several ways to jump between different headings in an org-mode file, depending on your preferred method:
	  
	  **Keyboard Shortcuts:**
	  
	  * **C-c C-n**: Jumps to the next visible heading.
	  * **C-c C-p**: Jumps to the previous visible heading.
	  * **C-c C-f**: Jumps to the next heading at the same level.
	  * **C-c C-b**: Jumps to the previous heading at the same level.
	  * **C-c C-u**: Moves up to the higher-level heading.
	  * **C-c C-j**: Opens a temporary buffer with the document structure, allowing you to navigate and select a specific heading using keys like TAB, UP/DOWN, and RET.
	  
	  **Search:**
	  
	  * **C-c g**: Activates the built-in search functionality, where you can type in the heading you want to find and jump to it directly.
	  * **M-x org-goto**: Opens the "org-goto" interface, which lets you select a heading from a list or search using keywords.
	  
	  **Other Options:**
	  
	  * **Outline view**: Use the outline view (C-o) to navigate through the headings visually and click on the desired one.
	  * **Helm/Ivy**: Some packages like helm-org-mode provide completion suggestions for headings, allowing you to quickly jump to them using fuzzy matching.
	  
	  **Additional Tips:**
	  
	  * You can customize the keybindings for these commands in your Emacs configuration file.
	  * The "org-goto-auto-isearch" variable controls whether the "org-goto" interface automatically searches for keywords as you type. You can turn it off for faster navigation using C-c g.
-