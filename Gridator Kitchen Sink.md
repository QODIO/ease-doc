# Gridator Kitchen Sink

#### Elements
* [Grid](#grid)
* [Block Grid](#block_grid)
* [Alert Boxes](#alert_boxes)
* [Breadcrumbs](#breadcrumbs)
* [Buttons](#buttons)
* [Buttongroups](#buttongroups)
* [Dropdown Buttons](#dropdown_buttons)
* [Split Buttons](#split_buttons)
* [Forms](#forms)
* [Video](#video)
* [Inline Lists](#inline_lists)
* [Keystroke](#keytroke)
* [Pagination](#pagination)
* [Panels](#panels)
* [Progress Bars](#progressbars)
* [Type](#type)
* [Blockquote](#blockquote)

&nbsp;
&nbsp;
## Grid
![Grid](https://github.com/ingipingi/Work/blob/master/images/grid.png)
```html
<div class="grid centered">
	<div class="row">
		<div class="column small-12">
			12
		</div>
	</div>
	<div class="row">
		<div class="column small-6">
			6
		</div>
		<div class="column small-6">
			6
			<div class="grid">
				<div class="row">
					<div class="column small-6">
						6
					</div>
					<div class="column small-6">
						6
					</div>
				</div>
			</div>
		</div>
	</div>
	<div class="row">
		<div class="column small-12">
			4
			<div class="grid">
				<div class="row">
					<div class="column small-6">
						4
					</div>
					<div class="column small-6">
						8
					</div>
				</div>
			</div>
		</div>
		<div class="column small-12">
			4
			<div class="grid">
				<div class="row">
					<div class="column small-6">
						3
					</div>
					<div class="column small-6">
						9
					</div>
				</div>
			</div>
		</div>
		<div class="column small-12">
			4
			<div class="grid">
				<div class="row">
					<div class="column small-6">
						3
					</div>
					<div class="column small-6">
						3
					</div>
					<div class="column small-6">
						6
					</div>
				</div>
			</div>
		</div>
	</div>
</div>
```

&nbsp;
&nbsp;
## Block-Grid
![Block-Grid](https://github.com/ingipingi/Work/blob/master/images/block-grid.png)
```html
<ul class="small-block-grid-2 large-block-grid-4 clearfix">
    <li>
        <img class="expand" src="/ease/images/browser_chrome.gif">
    </li>
    <li>
        <img class="expand" src="/ease/images/browser_opera.gif">
    </li>
    <li>
        <img class="expand" src="/ease/images/browser_safari.gif">
    </li>
    <li>
        <img class="expand" src="/ease/images/browser_firefox.gif">
    </li>
</ul>
```


&nbsp;
&nbsp;
## Alert Boxes
![Alert Boxes](https://github.com/ingipingi/Work/blob/master/images/alert-boxes.png)
```html
<div class="alert-box radius">
    This is a standard alert (div.alert-box.radius).
    <a href="#" class="close">×</a>
</div>
<div class="alert-box success">
    This is a success alert (div.alert-box.success).
    <a href="#" class="close">×</a>
</div>
<div class="alert-box alert round">
    This is an alert (div.alert-box.alert.round).
    <a href="#" class="close">×</a>
</div>
<div class="alert-box secondary">
    This is a secondary alert (div.alert-box.secondary).
    <a href="#" class="close">×</a>
</div>
```


&nbsp;
&nbsp;
## Breadcrumbs
![Breadcrumbs](https://github.com/ingipingi/Work/blob/master/images/breadcrumbs.png)
```html
<ul class="breadcrumbs">
    <li>
        <a href="#">Home</a>
    </li>
    <li>
        <a href="#">Features</a>
    </li>
    <li class="unavailable">
        <a href="#">Gene Splicing</a>
    </li>
    <li class="current">
        <a href="#">Cloning</a>
    </li>
</ul>
```

&nbsp;
&nbsp;
## Buttons (and busy buttons)
![Buttons](https://github.com/ingipingi/Work/blob/master/images/buttons.png)
```html
<div class="grid">
    <div class="row">
        <div class="small-12 large-6 column">
            <button class="tiny button">.tiny.button</button><br>
            <button class="small button">.small.button</button><br>
            <button class="button">.button</button><br>
            <button class="button expand">.expand</button><br>
        </div>
        <div class="small-12 large-6 column">
            <button class="tiny button secondary">.tiny.secondary</button><br>
            <button class="small button success radius">.small.success.radius</button><br>
            <button class="button alert round disabled">.round.disabled</button><br>
            <button class="button alert round" disabled>.round:disabled</button><br>
        </div>
    </div>
    <div class="row">
        <div class="small-12 large-6 column">
            <button class="tiny button busy">.tiny.button.busy</button><br>
            <button class="small button busy">.small.button.busy</button><br>
            <button class="button busy">.button.busy</button><br>
            <button class="button expand busy">.button.expand.busy</button><br>
        </div>
        <div class="small-12 large-6 column">
            <button class="tiny button secondary busy">.tiny.button.secondary.busy</button><br>
            <button class="small button success radius busy">.small.button.success.radius.busy</button><br>
            <button class="button alert round disabled busy">.button.alert.round.disabled.busy</button><br>
            <button class="button alert round busy" disabled>.button.round.busy:disabled</button><br>
        </div>
    </div>
</div>
```

&nbsp;
&nbsp;
## Button Groups
![Button Groups](https://github.com/ingipingi/Work/blob/master/images/buttongroups.png)
```html
<ul class="button-group split">
    <li>
        <button class="small button">Button 1</button>
    </li>
    <li>
        <button class="small button">Button 2</button>
    </li>
    <li>
        <button class="small button">Button 3</button>
    </li>
</ul>
<ul class="button-group split radius">
    <li>
        <button class="button secondary">Button 1</button>
    </li>
    <li>
        <button class="button secondary">Button 2</button>
    </li>
    <li>
        <button class="button secondary">Button 3</button>
    </li>
    <li>
        <button class="button secondary">Button 4</button>
    </li>
</ul>
<ul class="button-group split round">
    <li class="small-4">
        <button class="button expand alert">Button 1</button>
    </li>
    <li class="small-4">
        <button class="button expand alert">Button 2</button>
    </li>
    <li class="small-4">
        <button class="button expand alert">Button 3</button>
    </li>
</ul>
<ul class="button-group split round">
    <li class="small-4">
        <input type="submit" class="button expand success" value="Button 1">
    </li>
    <li class="small-4">
        <input type="submit" class="button expand success" value="Button 2">
    </li>
    <li class="small-4">
        <input type="submit" class="button expand success" value="Button 3">
    </li>
</ul>
```

&nbsp;
&nbsp;
## Dropdown Buttons
![Dropdown Buttons](https://github.com/ingipingi/Work/blob/master/images/dropdown-buttons.png)
```html
<button class="tiny button dropdown">Tiny Dropdown Button</button><br>
<button class="small secondary radius button dropdown">Small Secondary Radius Dropdown Button</button><br>
<button class="button alert round dropdown">Button Alert Round Dropdown Button</button><br>
<button class="large success button dropdown">Large Success Dropdown Button</button><br>
<button class="large button dropdown expand">Large Expanded Dropdown Button</button>
```

&nbsp;
&nbsp;
## Split Buttons
![Split Buttons](https://github.com/ingipingi/Work/blob/master/images/split-buttons.png)
```html
<button class="tiny button dropdown split">Tiny Split Button</button><br>
<button class="small secondary radius button dropdown split">Small Secondary Radius Split Button</button><br>
<button class="button alert round dropdown split">Round Alert Split Button</button><br>
<button class="large success button dropdown split">Large Success Split Button</button>
```

&nbsp;
&nbsp;
## Forms
![Froms](https://github.com/ingipingi/Work/blob/master/images/forms.png)
```thml
<form>
    <div class="grid">
        <div class="row">
            <div class="small-12 column">
                <label>Input Label</label>
                <input type="text" placeholder="small-12.column">
            </div>
        </div>

        <div class="row">
            <div class="small-12 medium-4 column">
                <label>Input Label</label>
                <input type="text" placeholder="small-12.medium-4.column">
            </div>
            <div class="small-12 medium-4 column">
                <label>Input Label</label>
                <input type="text" placeholder="small-12.medium-4.column" disabled value="disabled content">
            </div>
            <div class="small-12 medium-4 column">
                <label>Input Label</label>
                <ul class="input-group round">
                    <li class="small-9">
                        <input type="text" placeholder="li.small-9">
                    </li>
                    <li class="small-3">
                        <span class="postfix">.com</span>
                    </li>
                </ul>
            </div>
        </div>

        <div class="row">
            <div class="large-6 column">
                <label>Input Label</label>
                <input type="text" placeholder="large-4.column">
                <ul class="input-group round">
                    <li class="small-2">
                        <span class="prefix">http://</span>
                    </li>
                    <li class="small-8">
                        <input type="text" placeholder="small-9.column">
                    </li>
                    <li class="small-2">
                        <span class="postfix">.com</span>
                    </li>
                </ul>
            </div>
            <div class="large-6 column">
                <label>Input Label</label>
                <ul class="input-group round">
                    <li class="small-1">
                        <span class="prefix">$</span>
                    </li>
                    <li class="small-11">
                        <input type="text" placeholder="small-9.column">
                    </li>
                </ul>
            </div>
        </div>

        <div class="row">
            <div class="small-12 column">
                <label>Textarea Label</label>
                <textarea placeholder="small-12.column"></textarea>
            </div>
        </div>
    </div>
</form>
```

&nbsp;
&nbsp;
## Video
![Video](https://github.com/ingipingi/Work/blob/master/images/video.png)
```html
<div class="video" style="padding-top: 0; padding-bottom: 56%">
    <iframe src="//player.vimeo.com/video/93532909?title=0&amp;byline=0&amp;portrait=0&amp;color=b13438" width="500" height="281" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>
</div>
```

&nbsp;
&nbsp;
## Inline Lists
![Inline Lists](https://github.com/ingipingi/Work/blob/master/images/inline-links.png)
```html
<ul class="inline-list">
    <li><a href="#">Link 1</a></li>
    <li><a href="#">Link 2</a></li>
    <li><a href="#">Link 3</a></li>
    <li><a href="#">Link 4</a></li>
    <li><a href="#">Link 5</a></li>
</ul>
```

&nbsp;
&nbsp;
## Keystroke
![Keystroke](https://github.com/ingipingi/Work/blob/master/images/keystroke.png)
```html
To make something pretty, press and hold <kbd>cmd + alt + shift + w + a + !</kbd>
```

&nbsp;
&nbsp;
## Pagination
![Pagination](https://github.com/ingipingi/Work/blob/master/images/pagination.png)
```html
<ul class="pagination">
    <li class="arrow unavailable">
        <a href="">«</a>
    </li>
    <li class="current">
        <a href="">1</a>
    </li>
    <li>
        <a href="">2</a>
    </li>
    <li>
        <a href="">3</a>
    </li>
    <li>
        <a href="">4</a>
    </li>
    <li class="unavailable">
        <a href="">…</a>
    </li>
    <li>
        <a href="">12</a>
    </li>
    <li>
        <a href="">13</a>
    </li>
    <li class="arrow">
        <a href="">»</a>
    </li>
</ul>
```

&nbsp;
&nbsp;
## Panels
![Panels](https://github.com/ingipingi/Work/blob/master/images/panels.png)
```html
<div class="grid">
    <div class="row">
        <div class="medium-6 column">
            <div class="panel">
                <h5>This is a regular panel.</h5>
                <p>It has an easy to override visual style, and is appropriately subdued.</p>
            </div>
        </div>
        <div class="medium-6 column">
            <div class="panel red radius">
                <h5>This is a radius red panel.</h5>
                <p>It's a little ostentatious, but useful for important content.</p>
            </div>
        </div>
    </div>
    <div class="row">
        <div class="medium-6 large-4 column">
            <div class="panel yellow">
                <h5>This is a yellow panel.</h5>
                <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Harum, itaque.</p>
            </div>
        </div>
        <div class="medium-6 large-4 column">
            <div class="panel cyan radius">
                <h5>This is a radius cyan panel.</h5>
                <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Harum, itaque.</p>
            </div>
        </div>
        <div class="medium-12 large-4 column">
            <div class="panel purple">
                <h5>This is a purple panel.</h5>
                <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Harum, itaque.</p>
            </div>
        </div>
    </div>
    <div class="row">
        <div class="medium-6 column">
            <div class="panel green radius">
                <h5>This is a radius green panel.</h5>
                <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Harum, itaque.</p>
            </div>
        </div>
        <div class="medium-6 column">
            <div class="panel radius blue radius">
                <h5>This is a blue panel.</h5>
                <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Harum, itaque.</p>
            </div>
        </div>
    </div>
</div>
```

&nbsp;
&nbsp;
## Progressbars
![Progress Bars](https://github.com/ingipingi/Work/blob/master/images/progress-bars.png)
```html
<div class="progress medium-6">
    <span class="meter" style="width: 40%"></span>
</div>
<div class="radius progress success medium-8">
    <span class="meter" style="width: 80%"></span>
</div>
<div class="nice round progress alert medium-10">
    <span class="meter" style="width: 30%"></span>
</div>
<div class="nice secondary progress">
    <span class="meter" style="width: 50%"></span>
</div>
```


&nbsp;
&nbsp;
## Type
![Type](https://github.com/ingipingi/Work/blob/master/images/type.png)


&nbsp;
&nbsp;
## Blockquote
![Blockquote](https://github.com/ingipingi/Work/blob/master/images/blockquote.png)
```html
<blockquote>I do not fear computers. I fear the lack of them. Maecenas faucibus mollis interdum. Aenean lacinia bibendum nulla sed consectetur.<cite>Isaac Asimov</cite></blockquote>
```
