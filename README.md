function Superama(origin,destination) { //en donde dice superama van a cambiarlo por lo que sea.
  origin = "Av. del Servidor Público, Poniente, 45136 Zapopan, Jal." // aqui ponen su direccion.
  destination = "Superama Valle Real, Av Sta Margarita 4000, Poniente, 45136 Zapopan, Jal." // aqui el destino
  Logger.log(origin);
  Logger.log(destination)
  
  var directions = Maps.newDirectionFinder()
 .setOrigin(origin)
 .setDestination(destination)
 .getDirections();
 
  Logger.log(directions.routes[0].legs[0].distance.value);
  var km = directions.routes[0].legs[0].distance.value;
  var meters = km /1000;
  Logger.log(meters);
  return meters;
 }
