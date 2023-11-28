class Producto {
    var esNatural
    var suValoracion

    method suPrecio() {
     if(esNatural)
        return self.precioHabital() + 120
      else
         return self.precioHabital()
    }

    method precioHabital() = suValoracion * 30
}
class Macaron inherits Producto{
	var cobertura
	var suPeso
	var esEspecial
	
	method esEspecial(){
		return suPeso > 50 && cobertura 
	}
	
	method valoracion(){
	if(esEspecial)
		suValoracion = 120
	else
		suValoracion = 80
	}
}

class Alfajor inherits Producto{
	var pesoTapa
	var relleno
	var cantTapas
	
	method cualEsSuPeso(){
		return pesoTapa * cantTapas + relleno
		}
}

class MesaDulce{
	const productos = []
	
	method laMesaEsNatural(){
		return productos.any(esNatural)
	}
}
