Create two folders **public** and **src** then `npm install --save react react-dom react-router-dom`

**public**
	*./index.html* (simple html page but must have <div id="root"></div>)
**src**
	*./index.js* (Render to index.html <div> root)
```
import React from 'react';
import ReactDOM from 'react-dom';
import './index.css';
import * as serviceWorker from './serviceWorker';
import App from './components/App';

import Firebase, { FirebaseContext } from './components/Firebase';

ReactDOM.render(
	<FirebaseContext.Provider value={new Firebase()}>
		<App />
	</FirebaseContext.Provider>,
	document.getElementById('root'));
	
serviceWorker.unregister();
```
	
	./index.css
	./serviceWorker.js
	-components
		App
			./index.js (Consolidation of components via `import { BrowserRouter as Router, Route } from 'react-router-dom';` ** Import all routes exproted by routes.js)
		Component1
		Component2
		Component3
		...
	-constants
		./routes.js (export const NAME_OF_PAGE='/name_of_page')
