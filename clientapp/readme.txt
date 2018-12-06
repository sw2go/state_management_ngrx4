Um zu Debuggen:
---------------

.\server
VSCode "Debug"

.\client
ng serve
VSCode "Debug"


Erkenntnisse:
-------------

https://blog.nrwl.io/using-ngrx-4-to-manage-state-in-angular-applications-64e7a1f84b7b


backend.ts ist ein Angular Service mit Methoden zum Server-Backend
           findTalks, findTalk, rateTalk
           => alle geben Observables zurück

model.ts   definiert die Typen 
           der Backend Entitäten     => Talk, Filters
           den Status                => AppState, State
           die Actions               => TalksUpdated, TalkUpdated, Watch, TalkWatched, Rate, Unrate
           die Instanz des InitState => initState
           UND die Methode appReducer ( pure function ) 
	       diese erzeugt den neuen Status aufgrund des alten State und der Action
           UND die Klasse für die @Effects
               Effects sind Observables die Daten laden oder ändern 
               und bei Erfolg of() liefern falls die Action auch so zum Reducer soll
               oder eine neue Action liefern welche die Daten oder den Fehler melden





               


