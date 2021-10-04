# markdown-script

A new idea in enhancing markdown utilizing aliases and meta sections. Currently in design stage.

Markdown is very handy when it comes to situations where content is more important then presentation but presentation is still generally required to keep the content sensible.  Because markdown relies heavily of punctuation and simple patterns, the likelihood of undesired collisions between the markdown formatters and regular content becomes much greater.  One solution is to create a single enhancement which houses any possibility of other enhancements.  Something like a special block delimited for example by "@@@META" and terminated similarly.  Within the block configuration, enabling or disabling features, includes/embedding could happen that could be referenced outside the block.  An example of this might look something like...

```

@@@MDScript
import lib.github.plugins.named-anchors
load "section-one.md" as "{SECTION-ONE}" with named-anchors
load "section-two.md" as "{SECTION-TWO}" with named-anchors
@@@!
This document has 2 sections which outline a topic as [Section One](#SECTION-ONE} and [Section Two](#SECTION-TWO}.
# Section One
{SECTION-ONE}

# Section Two
{SECTION-TWO}
```

The above markdown would be rendered embedding external markdown files and auto generating named anchors at the beginning of the embedded content.  The rules are included before the use and made separate using  heredoc type syntax for the rules.  A simple level of logic and meta commands as a markdown script or mdscript could allow for multiple device and platform formatting. 

By leaving it to the editor what sort of enhancements they need and how they wish to define or include atop regular markdown.  This somewhat eliminates or at least reduces the inevitable chaos and corruption that ensues from people customizing markdown through their personal or common needs.   In this way we can keep a more basic and recognizable markdown syntax and any enhancements would be presented within the document so that editors ca more easily cater to their needs and not be bothered by enhancements that do not serve them or create additional problems.

In addition to embedding and rule declarations, inner blocks might also enable sections to be individually formatted or with their own rendering rules.  Thus allowing more control over the rendered content and introducing the potential for markdown to be used as a complete replacement for html and xml.  Why a replacement?  Well let's face it, HTML and XML are often overkill for many people requirements and a simpler set of styling and layout control could make presentation some more available to the common or non-HTML/non-CSS editor.  The concept of blocks as a requirment in markdown is certainly debatable, i am sure many will say if you need that much control of presentation then use HTML and CSS.  I don't disagree, but in the end it comes down to the ease or difficulty and the time it takes to implement and to manage the content.

Certainly much thought must be put into this project and a proper understanding of markdown and the popular flavors and variations to make this project worthwhile.

Have ideas?  Let me know.
