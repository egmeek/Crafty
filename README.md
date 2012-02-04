# Crafty JS
A JavaScript game engine. Uses jQuery like syntax for code organisation and conforming to
the Entity-Component-System paradigm. [Read this article for more information](http://cowboyprogramming.com/2007/01/05/evolve-your-heirachy/).

***

##Using Crafty
Game objects are divided into *Entities* and *Component*. Rather than the typical hierarchy, objects are composed of
functional components that augment the capabilities (sort of like adding classes to DOM elements).
<code>
    var player = Crafty.e();
	player.addComponent("2D, Gravity");
</code>

The above code will create a new entity then add two components labelled `2D` and `Gravity`. These components
will give the entity attributes and functions to extend its functionality. For example after adding the components
to the `player` entity, we can use a function provided by the `2D` component.
<code>
    player.attr({w: 50, h: 150}).area(); //will return 7500
</code>

In the code example we are setting the `width` and `height` properties inherited from the `2D` component. We can
then call the `area` method also inherited from the `2D` component.

##Developing

This is the workflow for committing to Crafty:

    git pull
    git checkout -b new-feature 
    # keep working on your feature till it's done 
    git pull
    git checkout develop 
    git merge --no-ff new-feature 
    git push origin develop 
    git branch -d new-feature 

If you don't have write access to the repo, please fork it and perform the same steps in your own repo. Then submit a pull request.

If this is causing you trouble, ask in the forums!