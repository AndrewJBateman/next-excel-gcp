# :zap: Next Excel GCP

* Next.js React used to connect to a GCP project excel sheet 'backend'
* **Note:** to open web links in a new window use: _ctrl+click on link_

![GitHub repo size](https://img.shields.io/github/repo-size/AndrewJBateman/next-excel-gcp?style=plastic)
![GitHub pull requests](https://img.shields.io/github/issues-pr/AndrewJBateman/next-excel-gcp?style=plastic)
![GitHub Repo stars](https://img.shields.io/github/stars/AndrewJBateman/next-excel-gcp?style=plastic)
![GitHub last commit](https://img.shields.io/github/last-commit/AndrewJBateman/next-excel-gcp?style=plastic)

## :page_facing_up: Table of contents

* [General info](#general-info)
* [Screenshots](#screenshots)
* [Technologies](#technologies)
* [Setup](#setup)
* [Features](#features)
* [Status](#status)
* [Inspiration](#inspiration)
* [Contact](#contact)

## :books: General info

* Text from Google Docs Sheet displayed in simple table.
* Includes navigation from title to content page
* There is no styling

## :camera: Screenshots

![Image of tech](./imgs/image.png)

## :signal_strength: Technologies

* [React v17](https://reactjs.org/) Javascript library.
* [Next v11](https://nextjs.org/) minimalist framework for rendering react apps on the server.
* [Google APIs Node.js Client npm module v78](https://www.npmjs.com/package/googleapis) client library for using Google APIs.
* [React dangerouslySetInnerHTML](https://reactjs.org/docs/dom-elements.html) "is React’s replacement for using innerHTML in the browser DOM. In general, setting HTML from code is risky because it’s easy to **inadvertently expose your users to a cross-site scripting (XSS) attack.** So, you can set HTML directly from React, but you have to type out dangerouslySetInnerHTML and pass an object with a __html key, to remind yourself that it’s dangerous."

## :floppy_disk: Setup

* Install dependencies using `npm i`
* Add GCP project credentials etc. as per tutorial
* `npm run dev` runs the Next app in the development mode. Open [http://localhost:3000](http://localhost:3000) to view it in the browser.
* `npm run lint` lints all files using ESLint - no warnings or errors

## :wrench: Testing

* N/A

## :computer: Code Examples

* function to display the posts with link to content page

```javascript
export default function Post({ posts }) {
	return (
		<article>
			<h1>Posts</h1>
			<ul>
				{posts.map((v, i) => (
					<li key={v}>
						<Link href={`/posts/${i + 2}`}>
							<a>{v}</a>
						</Link>
					</li>
				))}
			</ul>
		</article>
	);
}
```

## :cool: Features - Frontend

* Connecting to a GCP Docs Excel sheet using Next.js and not much code

## :clipboard: Status, Testing & To-Do List

* Status: Working
* To-Do: This could be expanded with pretty cards to display the data

## :clap: Inspiration

* [Fireship: Google Sheets… Your Next Database?](https://www.youtube.com/watch?v=K6Vcfm7TA5U)

## :file_folder: License

* N/A

## :envelope: Contact

* Repo created by [ABateman](https://github.com/AndrewJBateman), email: gomezbateman@yahoo.com
