use solana_program::{
    account_info::{next_account_info, AccountInfo},
    entrypoint,
    entrypoint::ProgramResult,
    msg,
    program::{invoke_signed},
    program_error::ProgramError,
    pubkey::Pubkey,
    rent::Rent,
    sysvar::Sysvar,
};

use spl_token::{
    instruction::{initialize_mint, transfer},
    state::Mint,
};

use std::convert::TryInto;

solana_program::declare_id!("YourProgramId11111111111111111111111111111111");

#[derive(Debug)]
pub enum Error {
    IncorrectProgramId,
}

impl From<Error> for ProgramError {
    fn from(e: Error) -> Self {
        match e {
            Error::IncorrectProgramId => ProgramError::Custom(0),
        }
    }
}

#[entrypoint]
pub fn process_instruction(
    program_id: &Pubkey, 
    accounts: &[AccountInfo], 
    input: &[u8]
) -> ProgramResult {
    Ok(())
}

fn initialize_mint_example(accounts: &[AccountInfo], decimals: u8) -> ProgramResult {
    let accounts_iter = &mut accounts.iter();
    let mint_account = next_account_info(accounts_iter)?;
    let rent_account = next_account_info(accounts_iter)?;

    let rent = &Rent::from_account_info(rent_account)?;

    let mint_authority = mint_account.key;

    let initialize_mint_ix = initialize_mint(
        &spl_token::id(),
        mint_account.key,
        mint_authority,
        None,
        decimals,
    )?;

    let seeds = &[&mint_account.key.to_bytes()[..32], &[mint_account.lamports.borrow_mut()]];
    let signer = &[&seeds[..]];

    invoke_signed(
        &initialize_mint_ix,
        &[mint_account.clone(), rent_account.clone()],
        signer,
    )?;

    Ok(())
}
