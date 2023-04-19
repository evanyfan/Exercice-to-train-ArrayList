# Exercice-to-train-ArrayList
In this exercice I training to use the ArrayList
package professorDisciplina;

import java.util.ArrayList;

public class Professor {
	private String nome;
	private String titulacao;
	private String departamento;
	ArrayList<Disciplinas> disciplinas; 
	//here we talk about the Array to use than in the code

	
	//  Constructor 
	public Professor (String nome, String titulacao, String departamento) {
		this.nome=nome;
		this.titulacao=titulacao;
		this.departamento=departamento;	
		this.disciplinas= new ArrayList<Disciplinas>();
	}
		
	
	// GETS it's the way to use the informations that.
    public String getnome() {
    	return nome;
    }
    public String titulacao() {
    	return titulacao;
    }
	public String departamento() {
		return departamento;
	}
		
		
	//SETS we use this to change the information that in the get's.
	 public void setnome (String newName) {
		 this.nome=newName;
	 }
	public void settitulacao(String newTitulacao) {
		this.titulacao=newTitulacao;
	}
     public void setdepartamento(String newDepartamento) {
    	 this.departamento=newDepartamento;
     }
     
    public void adicionarDisciplinas(Disciplinas d) {
    	this.disciplinas.add(d);
    }
    public void removerDisciplinas(String refCodigo){ 
    for (int i=0; i<this.disciplinas.size(); i++) {
    if (disciplinas.get(i).getCodigo().equals(refCodigo)){                        //.equals is the same than  == in py
    disciplinas.remove(i);}
    } 
    }
   
   public boolean alterarCh(String codeChangeTimeClass, int ch) {
	   for (int i=0; i< this.disciplinas.size();i++){
	   if (this.disciplinas.get(i).getCodigo().equals(codeChangeTimeClass)){
		   this.disciplinas.get(i).setch(ch);
		   return true;   
	   }	   
       } 
	   return false;
       }
    
}
