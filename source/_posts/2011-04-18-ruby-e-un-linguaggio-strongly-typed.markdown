---
comments: true
date: 2011-04-18 09:14:00
layout: post
slug: ruby-e-un-linguaggio-strongly-typed
title: Ruby è un linguaggio Strongly Typed
wordpress_id: 8
categories:
- Ruby &amp; RubyOnRails
---




Molti credono che ruby non sia un linguaggio tipizzato solo perche e dinamico. In realta dinamico non e in contrasto con tipizzato e un linguaggio dinamico puo essere strongly typed. Capiamo meglio.




In C#, che e un linguaggio statico, quando dichiaro il tipo di una variabile non posso cambiarlo. Ossia ho questo comportamento:



    
    int i = 3;



    
    i = "sono un linguaggio statico"; // errore: 



    
    <br></br>




in ruby invece posso cambiare il tipo della variabile:



    
    i = 3



    
    i = "sono un linguaggio dinamico"



    
    <br></br>




Siccome e un linguaggio dinamico il tipo di una variabile puo cambiare senza causare errori.




Questo pero non vuol dire che la variabile i non ha un tipo, ce l'ha ed e quello determinato dall'ultima operazione: prima e un Fixnum poi una stringa.







Ruby pero, come C#, e strongly typed, ossia questa operazione da un errore:






    
    i = 3



    
    i = i + "7" //TypeError: String can't be coerced into Fixnum







Quindi ruby ci permette di cambiare il tipo ad una variabile (dinamico) ma una volta definito il tipo le operazioni che possiamo fare sono limitate al tipo della variabile stessa (strongly typed).
