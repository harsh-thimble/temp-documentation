# Thimble UI Components Cheatsheet

This cheatsheet provides examples and descriptions of various components from the Thimble UI library. Feel free to copy and use the provided code snippets.

## Accordion

Accordion is a collapsible content container that allows you to show or hide sections of content.

**Attributes:**

* `title:`
* `description:`
* `index:`

```js
<Accordion title={"TITLE HERE"} description={"DESCRIPTION HERE"} index={1} >
  {ACCORDIAN CONTENT}
</Accordion>
```

## a or Link component

```txt
[LINK DISPLAY TEXT](<URL/LINK>)
```

## Button

A clickable button that performs an action when pressed.

**Attributes:**

* `text:`
* `bg:`
* `className:`
* `onClick:`

```tsx
<Button text='BUTTON TEXT' className='TAILWIND STYLING' bg='BACKGROUND COLOR' onClick={FUNCTION}/>
```

## BotAlert

A component that displays alerts or messages from a bot.

**Attributes:**

* `text:`

```tsx
<BotAlert text={"BOT ALERT TEXT CONTENT"} />
```

## Checkbox

A small box that can be selected or cleared to indicate a choice or option.

**Attributes:**

* `text:`
* `id (optional): `

```tsx
<Checkbox text={"TEXT CONTENT FOR THE CHECKBOX"} id={'SPECIFIER FOR THE CHECKBOX'}/>
```

## ChallengeCard

A card displaying a challenge with a title, description, and link for further information.

**Attributes:**

* `title:`
* `description:`
* `link:`
* `index (number):`

```tsx
<ChallengeCard title={'TITLE'} description={'DESCRIPTION'} link={'LINK'} index={INDEX} />
```

## code

A component that displays a block of code, possibly for programming lessons.

**Attributes / Place Holder:**

* `codelanguage:`
* `PROGRAM CODE:`

````tsx
```[codelanguage]
[PROGRAM CODE]
```
````

## ColWrapper

A component for organizing content in columns  (<u>Flex Container with flex-col type</u>).

**Attributes:**

* `children:`

```tsx
<ColWrapper>
  {children}
</ColWrapper>
```

## DocumentCard

A card which is a pdf viewer when the full screen icon is clicked.

**Attributes:**

* `image:`
* `link:`

```tsx
<DocumentCard image={'COVER IMAGE'} link={'LINK TO DOCUMENT/PDF'} />
```

## FlexWrapper

A flexible container for organizing content with customizable layout options.

**Attributes:**

* `type (optional):` 'row' (default) **OR** 'row-reverse' **OR** 'col' **OR** 'col-reverse'
* `align (optional):` 'center' (default) **OR** 'start' **OR** 'end' **OR** 'between' **OR** 'around' **OR** 'evenly' &#x20;
* `justify(optional):` 'center' (default) **OR** 'start' **OR** 'end' **OR** 'between' **OR** 'around' **OR** 'evenly' 
* &#x20;`wrap (optional):` 'wrap' (default) **OR** 'nowrap'
* `gap (optional):`x axis / horizontal gap (default '20px')
* `rowgap (optional):` y axis / vertical gap (default '20px')
* `children:`

```tsx
<FlexWrapper type={'TYPE'} align={'ALIGN'} justify={'JUSTIFY'} wrap={'WRAP'} gap={'GAP'} rowgap={'ROWGAP'}>{children}</FlexWrapper>
```

## FlashCards

A set of cards typically used for learning with quick, concise information.

**Attributes:**

* `title:`
* `description:`
* `index (number):`

```tsx
<FlashCards title='TITLE' description='DESCRITION' index={INDEX_NUMBER} />
```

## Gallery

A component for displaying a collection of images.

**Attributes:**

* `data:`Array of objects containing objects in order of the steps
  * `thumbnail:`Thumbnail size URL of the spotlight image
  * `image:`High resolution URL of the image on spotlight
  * `description (optional):`Description of the spotlight image
* `componentTitle:` Title of the entire gallery component

```tsx
<Gallery data=[
  {
    thumbnail: 'https://d2j2m4p6r3pg95.cloudfront.net/module_images/f2/22/f222b6ce0cec49e6ab541d9525322c39_thumb.jpg',
    image: 'https://d2j2m4p6r3pg95.cloudfront.net/module_images/f2/22/f222b6ce0cec49e6ab541d9525322c39_large.jpg',
    description: 'Some description here which is quite long',
  },
  {
    thumbnail:
    'https://images.unsplash.com/photo-1600058644245-ede8d11f6522?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=436&q=80',
    image:
    'https://images.unsplash.com/photo-1600058644245-ede8d11f6522?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=436&q=80',
  },
] componentTitle='componentTitle' />
```

## GridWrapper

A component for organizing content in a grid layout.

**Attributes:**

* `children:`
* `gap (optional):`x axis / horizontal gap (default '20px')
* `rowgap (optional):` y axis / vertical gap (default '20px')
* `col:`Specify the number of columns

```tsx
<GridWrapper gap={'GAP'} rowgap={'ROWGAP'} col={'NUMBER OF COLUMNS'}>
  {children}
</GridWrapper>
```

## hr

A horizontal line used to separate content.

```tsx
<hr/>
```

OR

```tsx
---
```

## h1, h2, h3, h4

Headings of different sizes used to structure and organize content hierarchically.

```tsx
<h1>{HEADING}</h1>
<h2>{HEADING}</h2>
<h3>{HEADING}</h3>
<h4>{HEADING}</h4>
```

**OR**

```tsx
# {HEADING 1}
## {HEADING 2}
### {HEADING 3}
#### {HEADING 4}
```

## IconButton

A clickable button with an associated icon.

**Attributes:**

* `journalLink:`Link to the journal file/pdf
* `notesLink:`Link to the notes file/pdf

```tsx
<IconButton journalLink={'journalLink'} notesLink={'notesLink'} />
```

## Image

A component for displaying images.

**Attributes:**

* `alt:`
* `src:`

```tsx
<Image
    alt={'TEXT TO SHOW IF IMAGE FAILS TO LOAD'}
    src={'URL OF THE IMAGE'}
  />
```

## ImageCard

A card displaying information along with an image.

**Attributes:**

* `title:`
* `image:`
* `description:`
* `index (number):`

```tsx
<ImageCard title={title} image={image} index={index} description={description} />
```

## IntroWrapper

A container for introductory content.

**Attributes:**

* `introduction:`It is an array of string where each string (each element of array) is an individual paragraph
* `children:`children contains the content which is shown side by side to the introduction content. It usually contains an image and BotAlert

```tsx
<IntroWrapper introduction={[INTRODUCTION_ARRAY]}>
{children} 
</IntroWrapper>
```

## KnowledgeCard

A card displaying information or knowledge.

**Attributes:**

* `title:`Title of the card
* `description:`Short description of the topic
* `link:` Link to the resource&#x20;
* `image:`Image URL/Link

```tsx
  <KnowledgeCard title={'CARD TITLE'} description={'DESCRIPTION TEXT'} link='LINK TO THE RESOURCE' image='IMAGE_LINK' />
```

## KnowledgeCheckBox

A checkbox associated with knowledge-related options.

**Attributes:**

* `data:`
  * `number:`Question Number
  * `type:`Question Type ('trueFalse' **OR** 'multipleChoice')
  * `question:`Question text
  * `options:`Array of string for options if ***'multipleChoice'***
  * `answer:`String if  ***'multipleChoice'*** else boolean (true | false) value
  * `weightage:`Marks for the particular question
  * `details:`Bot Alert  which shows description after a question is answered
* `onQuizComplete:`Function to run on quiz complete
* `setResult:`Function which sets result on quiz complete

```tsx
<KnowledgeCheckBox 
  data={[
    {
        number: 1,
        type: 'multipleChoice',
        question: 'What is the Creator Set Kit?',
        options: [
            'A set of books for creative writing',
            'A set of tools for building robots',
            'A set of components for building electronic devices',
            'A set of musical instruments for composing songs',
        ],
        answer: 'A set of components for building electronic devices',
        weightage: 5,
        details: 'The Creator Set Kit is a collection of components designed for building electronic devices.'
    },
    {
        number: 2,
        type: 'multipleChoice',
        question: 'What is the main function of the Arduino?',
        options: [
            'To store data',
            'To connect to the internet',
            'To control electronic components',
            'To play video games',
        ],
        answer: 'To control electronic components',
        weightage: 5,
        details: 'The main function of the Arduino is to control electronic components.'
    },
    {
        number: 3,
        type: 'multipleChoice',
        question: 'What is the Arduino IDE?',
        options: [
            'A coding language',
            'A circuit board',
            'A software program for programming the Arduino',
            'A set of tools for building robots',
        ],
        answer: 'A software program for programming the Arduino',
        weightage: 5,
        details: 'The Arduino IDE (Integrated Development Environment) is a software program used for programming the Arduino.'
    },
    {
        number: 4,
        type: 'multipleChoice',
        question: 'What is a circuit?',
        options: [
            'A type of game',
            'A path for electrical current to flow',
            'A type of robot',
            'A type of musical instrument',
        ],
        answer: 'A path for electrical current to flow',
        weightage: 5,
        details: 'A circuit is a path through which electrical current can flow.'
    },
    ]}
    onQuizComplete={() => {}}
    setResult={() => {}}
/>
```

## Lists

Components for creating ordered and unordered lists.

**Unordered List (UL)**

```tsx
- List item 1
- List item 2
```

**Ordered List (OL)**

```tsx
1. List item 1
2. List item 2
```

## ResourceCard

A card displaying information about a learning resource, possibly a file.

**Attributes:**

* `src:`
* `title:`

```tsx
<ResourceCard src={'URL OF IMAGE'} title={'CONTENT DESCRIPTION OF IMAGE/RESOURCE'} />
```

## RowWrapper

A component for organizing content in rows (<u>Flex Container with flex-row type</u>).

**Attributes:**

* `children:`

```tsx
<RowWrapper>
    {children}
</RowWrapper>
```

## SectionCard

A card associated with a section, typically used for navigation.

**Attributes:**

* `index:`Number between 1-4 to set different colors to the card
* `title:`
* `title:`
* `title:`

```tsx
<SectionCard title={'CARD TITLE'} body={'CARD CONTENT'} index={1-4} url={'LINK TO PAGE'} />
```

## Slider

A component showing a list of images and a spotlight image with description.

**Attributes:**

* `data:`Array of objects with following data type
  * `thumbnail:`Thumbnail size URL of the spotlight image
  * `image:`High resolution URL of the image on spotlight
  * `description (optional):`Description of the spotlight image

```tsx
<SliderComponent data={data} />
```

## Steps

A component for displaying a series of steps or instructions.

**Attributes:**

* `data:`Array of objects containing objects in order of the steps
  * `title:`Title/heading for the step
  * `description:`Description for the step explaining the process
  * `image:`Image link describing that step
  * `tootltip:`A pop-up providing brief information on hover.
* `componentTitle:` Title of the entire step component

```tsx
<Steps
        data={[
    {
        "title": "Gather the Project Components",
        "description": "Gather your Arduino, Base Shield, (1) Cable, LED Driver, and (1) LED in a color of your choice.",
        "image": "https://cdn.thimble.io/assets/curriculum/creator-set-playground/Step 1 - Gather Components.png",
        "tooltip": "Just so you know, we’ll be using a red LED!"
    },
]
}
        componentTitle={'TITLE FOR THE STEPS COMPONENT'}
    />            
</div>
```

## TeacherOnly

A component that displays content only for teachers.

**Attributes:**

* `role:`
* `children:`

```tsx
<TeacherOnly role={'ROLE'}>
     {children}
</TeacherOnly>
```

## ToolTip

A small pop-up box displaying additional information when hovering over an element.

**Attributes:**

* `text:`Text to show on tooltip hover
* `id:`Tooltip ID
* `children:`Content / Icon which when hovered shows the tooltip

```tsx
<ToolTip text={"TEXT TO SHOW ON HOVER"} id={'ID FOR THE TOOLTIP'} >
  {children}
</ToolTip>
```

## VideoPlayer

A component for playing videos.

**Attributes:**

* `thumbnail:`Thumbnail image link
* `link:`Link to the vider

```tsx
<VideoPlayer thumbnail={'THUMBNAIL LINK'} link={'URL OF THE VIDEO'} />
```