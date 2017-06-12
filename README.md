# Eclipse tm4e - TextMate support in Eclipse IDE

[![Eclipse License](http://img.shields.io/badge/license-Eclipse-brightgreen.svg)](https://github.com/eclipse/tm4e/blob/master/LICENSE)
[![Build Status](https://secure.travis-ci.org/eclipse/tm4e.png)](http://travis-ci.org/eclipse/tm4e)

`tm4e` provides the capability to support TextMate tokenizer with Java and integrates it with Eclipse IDE.

`tm4e` is an [official Eclipse.org project](https://projects.eclipse.org/projects/technology.tm4e) so it conforms to typical Eclipse.org requirements and guarantees.

## Install

You can install `tm4e` with the update site `http://download.eclipse.org/tm4e/snapshots/` which provides samples of syntax coloration with:

 * GenericEditor for Language Server (C#, CSS, JSON)
 * a TypeScript Editor.

## Code

It provides:

 * [org.eclipse.tm4e.core](https://github.com/eclipse/tm4e/tree/master/org.eclipse.tm4e.core) provides the Java TextMate tokenizer. This project is a Java port of [vscode-textmate](https://github.com/Microsoft/vscode-textmate) written in TypeScript. This Java API can be used with any Java UI Toolkit (Swing, Eclipse, etc). See [Core](https://github.com/eclipse/tm4e/wiki/Core) section for more information.

 * [org.eclipse.tm4e.ui](https://github.com/eclipse/tm4e/tree/master/org.eclipse.tm4e.ui) provides the Eclipse **org.eclipse.jface.text.presentation.IPresentationReconciler** [TMPresentationReconciler](https://github.com/eclipse/tm4e/blob/master/org.eclipse.tm4e.ui/src/main/java/org/eclipse/tm4e/ui/text/TMPresentationReconciler.java) which is able to tokenize an editor content by using a given JSON, PList TextMate grammar and do syntax coloration. See [UI](https://github.com/eclipse/tm4e/wiki/UI) section for more information.

Here a sample with TypeScript:

![TypeScript Editor](https://github.com/eclipse/tm4e/wiki/images/TypeScriptEditor.png)


## Get support and contribute

* **License and community**: `tm4e` is a community open-source project licensed under the Eclipse Public License 1.0.
* **Support:** You can ask questions, report bugs, and request features using [GitHub issues](http://github.com/eclipse/tm4e/issues).
* **Git**: This `eclipse/tm4e` repository is the reference repository to contribute to `tm4e`
* **Build and CI**: build can be performed with a simple `mvn clean verify`, continuous integration and deployment is performed by CI jobs at https://hudson.eclipse.org/tm4e
* **Developers mailing-list**: Contributors are also expected to subscribe the [tm4e-dev mailing-list](https://dev.eclipse.org/mailman/listinfo/tm4e-dev).
* **Becoming a committer**: as usual with Eclipse.org projects, anyone who's made significant contributions and who

## Setting up TM4E for development

After downloading the sources from the github repo, to get the environment, two .target definition files
are provided at /tm4e/target-platform -- open the selected file inside Eclipse and click
"Set as Target Platform" (note that this folder isn't configured as a project, so, it has to be
opened through File > Open).

The `tm4e-target.target` provides a target which allows running TM4E (to be used if you're only
interested in running TM4E) and `running-platform-plus-tm4e.target`, which provides a target that
has the current running platform and TM4E (to be used if you are also developing
other plugins which require the current target platform).

